## Généralité
Le backend (API) de Démonette permet de communiquer avec directement avec la base de données Elastic de la stack Démonette.
Elle permet entre autres d'effectuer des recherches et de construire les données néccéssaires pour construire les graphes dans 
le frontend (algorithme présent dans le fichier `methods/graph.js`)

## Dépendance
- Node.js (Express.js)
- dépendance dans le `package.json`

## Comment démarrer le serveur ?

`npm start ELASTIC_DEMONETTE=$ELASTIC_DEMONETTE URL_ROOT_PATH=$URL_ROOT_PATH PREFIX=$PREFIX`

- ELASTIC_DEMONETTE : url de la base Elastic
- URL_ROOT_PATH : racine de l'application web
- PREFIX : (Cyril ?)
