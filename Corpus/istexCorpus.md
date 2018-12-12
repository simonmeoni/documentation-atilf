## Généralité

Ce corpus est un sous-corpus d'ISTEX sur le thème du vieillissement, il regroupe 8807 fichiers sur ce thème. Ils sont au formats TEI/XML

## Arborescence
Voici les plusieurs dossiers du projet et ce qu'il contient : 

- `tei` : les fichiers ne sont pas modifiés de manière particulière, ils sont dans l'état après extraction de la base ISTEX
- `tei_force` : les fichiers `xml` sont aux formats TEI mais le header a été supprimé pour pouvoir passer l'étape de validation avec le `rnc` tei_all
- `tei_force_only, tei_force_only, tei_force_tiny`: les corpus contiennent un nombre restreint de fichiers pour pouvoir effectuer des test, ils n'ont pas de header
-  `tei_normalize`: avant de pouvoir enlever le header, on ajoute dans le namespace tei afin de pourvoir effectuer l'étape de suppression de header.

donc le procédure fonctionne comme cela : tei --> normalize.rb --> tei_normalize --> force_validate.rb --> tei_force --> déplacement manuel vers le autres dossiers

## Lien vers le projet 
[https://git.atilf.fr/corpus/istext-corpus](https://git.atilf.fr/corpus/istext-corpus)