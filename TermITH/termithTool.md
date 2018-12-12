## Généralité
TermITH tool est un ensemble de scripts et de feuilles XSL permettant l'enrichissement de document XML/TEI tout comme TermITH-java.
La différence est qu'il a aussi pour fonction de mettre en conformité l'ancienne version du corpus TermITH.  
## Dépendance et Langage utilisé
- XSLT 1.0/2.0
- Python
- Java
- Termsuite 2.2
- TreeTagger
- Bash
## I/O

- Entrée : l'ensemble du corpus TermITH en XML qui n'est pas en conformité avec le format actuel. Ce corpus n'est pas enrichi.
- Sortie : le corpus termITH dans sa nouvelle mouture, il est aussi enrichi avec un ensemble couches d'annotations morhpo-syntaxique, terminologique ainsi que la projection des ressources phraséologique et transdisciplinaire..


## Liens vers le projet
[https://git.atilf.fr/termith/termITH-tool](https://git.atilf.fr/termith/termITH-tool)