## Généralité
Cette application permet de d'injecter dans la base SQL, la ressource Phraseo et le LST du LIDILEM.
Mais attention, ce script est à nettoyer car il n'y a aucune variable d'environnement, aucune CLI pour le réexecuter sur une autre machine que la mienne  

## Dépendance et Langage utilisé
- python
- TreeTagger
- bibliothèque python : lxml, MySQLdb, json
 

## I/O

- Entrées : Le json du lexique transdisciplinaire, la ressource phraseo en XML
- Sorties : la base lexique enrichie

## Liens vers le projet
[https://git.atilf.fr/corea2d/lst-converter](https://git.atilf.fr/corea2d/lst-converter)