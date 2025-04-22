# 1. Introduction au cours

## Introduction 

Ce cours fait suite au cours "Data Science pour la Finance", ayant pour but d'introduire un certain nombre de concept de Machine Leaning, Data Science et modélisations statistiques appliqués au domaine de la banque et de l'assurance. 

Dans ce cours, dispensé par Zacharie BUISSON & Mario DEFRANCE, vous apprendrez les bases de l'ingéniérie logicielle appliqué au Machine Learning. En gros, nous verrons ensemble comment faire en sorte qu'un modèle learning puisse être utilisé en dehors de son propre PC, comment le maitriser et le suivre au travers du temps.

Normalement, ce cours donnera une vision plus globale sur ce qu'il se passe une fois que l'on a réussir des probabilités avec un modèle de Machine Learning, et comment les utilisateurs finaux peuvent utiliser ce que l'on produit. A la fin de ce cours, vous avez été capables de constuire un modèle de Machine Learning sur des données réelles et d'en mesurer les performances.

L'aventure liée à ce modèle n'est pas encore finie ! Maintenant que ce modèle a été développé sur votre ordinateur, il est temps de le rendre disponible à la terre entière :)

## Objectif de ce cours

L'objectif de ce cours est donc de rendre disponible le modèle en le mettant en production. Ce cours proposera donc une introduction à la construction et le déploiement d'une telle solution, ainsi que d'un grand nombre d'enjeux liés à ce sujet.

Ce cours abordera donc la création d'un système de mise à disposition d'un modèle de Machine Learning par la création d'une application associée (API - Application Programing Interface). Cette application sera ensuite déployée en production sur des environnements adaptés encapsulé dans une image Docker elle même déployée et configurée en production par des fichiers de Configuration kubernetes. 

Ces travaux sont l'occasion de (re)découvrir tout un ensemble de bonnes pratiques MLOps. Ces bonnes pratiques sont essentielles à la bonne réalisation d'un projet de Data Science et permettront d'apporter une vision opérationnelle à vos futurs projets en entreprise.

## Présentation de la structure de ce cours

Ce cours se divise en deux parties : 
- une première aprtie théorique (environ une matinée) qui sera constituée d'une présentation des concepts majeurs de l'ingéniérie logicielle appliquée au Machine Learning ;
- un TD : nous appliquerons les grands concepts au modèle de ML que vous avez construits au précédent module.

Sur la partie cours, il y a un powerpoint qui contient un condensé de ce que l'on peut savoir basiquement sur le sujet, et un cours résumé et écrit sur GitHub qui est en fait un grand tutoriel de comment bien construire une application de ML pour la production.

Vous êtes le premier groupe à suivre ce cours : n'hésitez pas à nous faire un retour si cela n'a pas déjà été fait, au moins sur la partie théorique.

## Notation et évaluation

Comme dit précédemment, le but de ce cours est de construire une application qui découle de notre modèle de Machine Learning : 


| **Catégorie**                        | **Éléments**                            |
|-------------------------------------|-----------------------------------------|
| **Factorisation du code (script) - 5 pts**  | - Code mis sous forme de fonctions <br>  - Code clair <br> - Respect de la qualité du code Python <br> - Tests unitaires pertinents pour chaque fonction |
| **Application API - 5 pts**                     | - Développement de l'API (health_check, predict...) <br> - Création d'une documentation <br> - Test de l'application en local |
| **CI/CD et Déploiement - 5 pts**            | - Intégration continue (CI) en place <br> - Déploiement continu (CD) en place <br> - Image disponible sur le registry <br> - Application déployée en ligne |
| **Mise en perspective de l'application - 5 pts** | - Description de l’application <br> - Méthode pour mesurer l’impact du modèle <br> - Stratégie de tests en production <br> - Bonnes pratiques de MLOps supplémentaires |

## Prérequis pour ce cours 

Pour suivre ce cours, vous aurez besoin de :
- créer un compte GitHub ;
- créer un compte RedHat developer (une note de procédure est dispo ici : lien) ;
- utiliser un IDE en local (Visual Studio Code, Pycharm...)