## Généralité
Cette application permet, depuis des requêtes sur la base sql lexique, de
créer les fichiers json, xml des ressources lexicales Phraseo et LST. 
## Dépendance et Langage utilisé
- python
- bibliothèque python : lxml, MySQLdb, json, click
 

## I/O

- Entrées : aucune
- Sorties : en fonction des options sélectionnées on peut avoir des fichiers xml ou json

## Comment éxéctuter le programme ?
- `python phraseoLstSerializer.py json lexique_transdisciplinaire` : permet de générer le lst au format json

    **ou**

- `python phraseoLstSerializer.py xml lexique_transdisciplinaire` : permet de générer le lst au format xml

    **ou**

- `python phraseoLstSerializer.py xml lexique_phraseo` : permet de générer la ressource phraseo au format xml

    **ou** 

- `python phraseoLstSerializer.py json lexique_phraseo` : permet de générer la ressource phraseo au format json
 
## Liens vers le projet
[https://git.atilf.fr/corea2d/lst-converter](https://git.atilf.fr/corea2d/lst-converter)