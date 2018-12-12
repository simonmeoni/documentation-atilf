## Généralité
stdfSpec est un projet permettant de générer le schéma Relax-NG du format standOff/TEI.
Ce format est utilisé pour le corpus TermITH et dans l'application TermITH-java.
 
## Qu'est-ce que le format Standoff/TEI ?
C'est un format d'annotations sous forme d'un module pour le format TEI, chaque couche d'annotation est contenu dans une balise `ns:standOff`.
Dans le cas de termITH, le texte présent dans la balise `<body>` est tokénisé (à l'aide de treeTagger) puis indexé à l'aide d'`xml:id`.
Le report de ces id dans les couches d'annotations permet d'effectuer des analyses morpho-syntaxiques ou sémantiques.
Voici les couches d'annotations présentes : 
1. annotation morpho-syntaxique et lemmatisation (à l'aide de treeTagger) (identifié avec la balise `<ns:standOff type='wordForms>'`)
2. candidats termes (identifié avec la balise `<ns:standOff type='candidatsTermes>'`)
3. phraséologie (identifié avec la balise `<ns:standOff type='phraseologie>'`)
4. lexiques Transdisciplinaire (identifié avec la balise `<ns:standOff type='lexiquesTransdisciplinaires>'`)
5. Indexation effectué par le labo de Nantes (mais on s'en sert pas vraiment et on ne maîtrise pas le contenu dedans ), (identifié avec la balise `<ns:standOff type='Indexation'>`)

## Le schéma
Le schéma est présent dans le dossier testStandOffWithTBX/standOffWithTBX.rnc
Pour le générer on utilise l'outil en ligne [ROMA](http://roma.tei-c.org/), il faut uploader le `.odd` dans l'interface web et c'est bon !
Mais je suis assez optimiste vis à vis de ce point (j'ai mis un peu de temps avant de comprendre le format odd et l'interface est assez compliqué), je pense qu'il faut demander de l'aide à Bertrand au préalable pour des modifications du fichier `.odd`.

**NORMALEMENT IL N'Y A PAS BESOIN DE MODIFIER LE FORMAT. DANS LE CAS CONTRAIRE, ÇA IMPLIQUE DE FAIRE DES MODIFICATIONS DANS TOUS MES PROJETS DONC C'EST DANGEREUX**

## Liens vers le projet
[https://git.atilf.fr/termith/stdfSpec](https://git.atilf.fr/termith/stdfSpec)