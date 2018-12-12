## Généralité
le projet démondette contient l'ensemble des fichiers permettant de déployer la stack de l'application web démonette,
cette stack se compose de 3 éléments : 
1. le front de démonette (demonette-frontend)
2. le back de démonette (demonette-backend)
3. le déploiement de la base de données (`Elastic`) constitué de la ressource lexicale démonette (`CSV`). Chaque ligne du CSV étant 
une entrée de la base `Elastic`.

## Accès à l'application web
Le déploiement en intégration continu utilise le fichier docker-stack-compose.int.yml et est accessible à l'adresse : http://demonette-int.atilf.fr/. Pour le lancer, il faut commiter dans le master des sous projets ou lancer le pipeline à partir de la branche master.
Le déploiement en producction utilise le fichier docker-stack-compose.prod.yml et est accessible à l'adresse : https://demonette.atilf.fr/. Pour le lancer, il faut merger la branche master dans production.
