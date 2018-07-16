# Long parameter List

## Symptomes

Plus de 3 ou 4 paramètres pour une méthode

## L'origine du problème

Une longue liste de paramètres est souvent le résultat de plusieurs comportements qui ont été regroupés au sein d'une même méthode.

## Correction

Vérifier les paramètres passés. Si certains sont le résutlat d'une méthode d'un autre objet, utiliser __Replace Parameter with Method Call__
- Au lieu de passer un group de données reçu d'un autre object, passer l'objet lui même en paramètre de la méthode, en utilisant __Preserve Whole Object__
- Si les paramètres ne sont pas reliés par un objet, il est parfois possible de les mettre dans un même objet en utilisant __Introduce Parameter Object__

## Résultat

- Lisibilité accrue, code plus succinct
- Le refactoring peut mettre en évidence de la duplication de code

## Quand ignorer

Ne vous débarassez pas des paramètres si cela entraine l'apparition d'un dépendance non souhaitée.
