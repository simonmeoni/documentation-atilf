## Généralité
xlo est un wrapper pour rnv et xmllint qui permet de fusionner les différentes erreurs dans un fichier `csv`

## Dépendance et Langage utilisé
- ruby 2.5
- xmllint
- rnv

## Liens utiles
- [http://www.davidashen.net/rnv.html](http://www.davidashen.net/rnv.html)
- [http://rubygems.org/gems/xlo](http://rubygems.org/gems/xlo)

## Installation
1. gem install xlo
2. apt-get install rnv
3. apt-get install xmllint
4. xlo start rnc-schema xml-folder

## I/O
- Entrées : des fichiers XML et le schema `.rnc` qui permettant de tester la validitié de l'ensemble des fichiers `xml`. 
- Sorties : un fichier `csv` contenant l'ensemble des erreurs xmllint/rnv

## Docker
1. `docker run -t -v $HOST_PATH$:/input --name xlo_docker registry2.atilf.fr/termith/xlo:master`
2. `docker exec xlo_docker xlo start -s relative/path/schema/tei-all.rnc -i relative/path/folder/with/xml`

## Liens vers le projet
[https://git.atilf.fr/termith/xlo](https://git.atilf.fr/termith/xlo)