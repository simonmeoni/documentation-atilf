## Généralité

- Démonette injector est un script python permettant d'injecter dans une base Elastic Search l'ensemble des données de la ressource lexicale de Démonette 
(qui correspond au fichier CSV).
Chaque ligne du csv correspond à une entrée de la base.

## Dépendances

- pythton 3.6
- bibliothèque néccéssaire : click, elastic

## Comment rajouter des entrées dans la base démonette pour qu'elles soient visible sur l'interface client ?

1. modifier la base, ajouter des entrées
2. faire un commit et pousser sur le repository (selon la méthode gitflow)
3. ensuite il faut modifier les caractéristiques visibles (correspondant aux variables `res` ) des entrées dans les fichiers suivants du projet démonette-frontend:
  - demonette-frontend/src/methods/formatPhoneticRequest.js
  - demonette-frontend/src/methods/formatAggregation.js
4. puis commiter, pusher sur le projet démonette-frontend (selon la méthode gitflow)



