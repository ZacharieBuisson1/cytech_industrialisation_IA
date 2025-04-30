# Test the API in local

### Lancer l'application en local sur son poste 

Vous pouvez lancer une API directement en local avec votre propre poste.

L'application exposera alors les routes que vous avez développées. Pour cela, normalement, il suffit de lancer l'API avec uvicorn, et elle sera fonctionnelle.

```bash
uvicorn run api:app
```

*Remarque : Uvicorn est un package à installer avec Poetry...*

### Comment tester son application en local sur son poste ? 

Pour tester une application en local sur son poste, il est possible d'exécuter  avec une requête du style : 

curl -X POST http://127.0.0.1:8000/predict -H "Content-Type: application/json" -d your_data_in_json.

