## Généralité
L'application RLF to Brat permet de convertir les exemples du RLF pour un vocable donnée vers le format de la plateforme d'annotations Brat  

## Dépendance et Langage utilisé
- Ruby 2.5
- les dépendances sont dans le gemfile mais ce fichier doit être nettoyé

## I/O

- Entrées : la base du RLF au format `csv`
- Sorties : Deux dossiers :
    1. un dossier contenant les exemples déjà annotés du RLF contenant les `.ann`, les `.txt` et le schéma d'annotation généré automatiquement (`.conf`)
    1. un dossier contenant les exemples à annoter du RLF contenant les `.ann`, les `.txt` et le schéma d'annotation généré automatiquement  (`.conf`)

## Liens vers le projet
[https://git.atilf.fr/corea2d/rlf-to-brat](https://git.atilf.fr/corea2d/rlf-to-brat)