# Refactoring du preprocessing

### A propos de la réécriture d'un preprocessing entrainé

Il a été évoqué pendant le TD la nécessité de sauvegarder un preprocessing qui nécéssite un entrainement. Donnons un exemple :

```python
def nan_remover(df.pandas.DataFrame, threshold:float=0.9):
    col_to_drop = []
    for col in df.columns.tolist():
        if df[col].isna().mean() > threshold:
            col_to_drop.append(col)
    return col_to_drop
```

Ce preprocessing a besoin d'apprendre : il doit déduire des données d'apprentissage les colonnes sur lesquelles une opération est nécessaire. Ce préprocessing ne peut pas être mis tel quel dans le code de production, car il suppremerait toutes les colonnes avec des valeurs manquantes et ne serait pas iso avec le train.

Deux méthodes s'offrent naturellement à nous :

##### Méthode 1 - Sauvegarder la liste des valeurs à supprimer en dur

On peut décider de sauvegarder les colonnes à drop ou les informations d'un processing à entrainer (valeurs, liste de colonnes).

```python
with open("list_info_train.pkl", "wb") as f:
    pickle.dump(list_col_to_remove, f)
```

Cette méthode est lourde car il faut précisément tracer l'ensemble des étapes de modélisation.

##### Méthode 2 - Créer une étape de Pipeline sklearn à entrainer 

La méthode la plus propre est de créer une classe python qui fait ça : 

```python
from sklearn.base import BaseEstimator, TransformerMixin
import pandas as pd

class NanRemover(BaseEstimator, TransformerMixin):
    def __init__(self, threshold=0.9):
        self.threshold = threshold
        self.columns_to_remove = []

    def fit(self, X, y=None): # nom de fonction obligatoire pour entrainer
        self.columns_to_remove = [
            col for col in X.columns if X[col].isna().mean() > self.threshold
        ]
        return self

    def transform(self, X): # nom de fonction obligatoire pour appliquer
        return X.drop(columns=self.columns_to_remove, errors='ignore')
```

Ce format est plus propre et plus complet, et il peut être intégrer dans le cadre d'une pipeline sklearn.