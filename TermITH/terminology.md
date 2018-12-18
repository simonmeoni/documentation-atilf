## Généralité
Ce projet est un ensemble de script utilisé pour l'article dans la revue Terminology. Dans cette expérimentation, on essaie de comparer les méthodes de désamb utilisé par 
le LINA, le LORIA et l'ATILF. L'ensemble des scripts ne sont pas très réutilisables (ils effectuent tous des tâches très très spécifiques) mais peuvent être utile pour des expérimentations similaires à la rigueur.
## Dépendance et Langage utilisé
- Ruby
- Bibliothèque Ruby utilisé : Nokogiri

## I/O

- Entrées : des fichiers XML à peu près au [format pivot](TermITH/stdfSpec.md)
- Sorties : trois fichier `csv` qui décrivent l'ensemble des expérimentations effectués (Rappel, Précisions, F-mesure) par les trois méthodes des trois labo

## Docker
Ce projet n'est pas dockérisé (cf **Généralité**)

## Liens vers le projet
[https://git.atilf.fr/termith/terminology](https://git.atilf.fr/termith/terminology)