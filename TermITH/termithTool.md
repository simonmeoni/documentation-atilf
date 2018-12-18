## Généralité
TermITH tool est un ensemble de scripts et de feuilles XSL permettant l'enrichissement de document XML/TEI tout comme TermITH-java.
La différence est qu'il a aussi pour fonction de mettre en conformité l'ancienne version du corpus TermITH à l'aide de feuille xsl  au [format pivot](TermITH/stdfSpec.md).
Les feuilles XSL de mises en conformité sont executés à l'aide de script bash, voici l'ensemble de ces scripts : 
 - [https://git.atilf.fr/termith/termITH-tool/blob/master/scripts/sh/phase1-norm-tei-alldata.sh](https://git.atilf.fr/termith/termITH-tool/blob/master/scripts/sh/phase1-norm-tei-alldata.sh)
 - [https://git.atilf.fr/termith/termITH-tool/blob/master/scripts/sh/phase2-supp-apos-alldata.sh](https://git.atilf.fr/termith/termITH-tool/blob/master/scripts/sh/phase2-supp-apos-alldata.sh)
 - [https://git.atilf.fr/termith/termITH-tool/blob/master/scripts/sh/phase3-supp-biblio-alldata.sh](https://git.atilf.fr/termith/termITH-tool/blob/master/scripts/sh/phase3-supp-biblio-alldata.sh)
 - [https://git.atilf.fr/termith/termITH-tool/blob/master/scripts/sh/phase4-mettre-note-fin-alldata.sh](https://git.atilf.fr/termith/termITH-tool/blob/master/scripts/sh/phase4-mettre-note-fin-alldata.sh)
 - [https://git.atilf.fr/termith/termITH-tool/blob/master/scripts/sh/phase5-mettre-commentaire-alldata.sh](https://git.atilf.fr/termith/termITH-tool/blob/master/scripts/sh/phase5-mettre-commentaire-alldata.sh)
 - [https://git.atilf.fr/termith/termITH-tool/blob/master/scripts/sh/phase6-modifier-unicode-alldata.sh](https://git.atilf.fr/termith/termITH-tool/blob/master/scripts/sh/phase6-modifier-unicode-alldata.sh)
## Dépendance et Langage utilisé
- XSLT 1.0/2.0
- Python
- Java
- Termsuite 2.2
- TreeTagger
- Bash
## I/O

- Entrée : l'ensemble du corpus TermITH en XML qui n'est pas en conformité avec le [format pivot](TermITH/stdfSpec.md). Ce corpus n'est pas enrichi.
- Sortie : le corpus termITH dans sa nouvelle mouture, il est aussi enrichi avec un ensemble couches d'annotations morhpo-syntaxique, terminologique ainsi que la projection des ressources phraséologique et transdisciplinaire..


## Liens vers le projet
[https://git.atilf.fr/termith/termITH-tool](https://git.atilf.fr/termith/termITH-tool)