# Feature Envy

## Symptomes

Une méthode qui accède aux données d'un autre objet plus qu'à ses propres données.

## L'origin du problème

Ce problème peut arriver lorsque que les données sont migrées vers une data class. Quand c'est le cas il est souhaitable de déplacer cette fonction dans l'objet contenant les données.

## Correction

Ce qui évolue en même temps devrait être rassemblé dans un même endroit. Généralement des données et méthodes qui les utilisent sont modifiés au même moment.

- Si une appartient clairement à une autre classe, on peut utiliser __Move Method__.
- Si seulement une partie de la method accède aux données d'un autre objet, utiliser __Extract Méthode__ pour migrer cette partie vers cet objet.
- Quand une méthode utilise plusieurs fonction d'un autre classe, dabord déterminer quelle est la classe qui contient la plus grande partie des données utilisées. Placer ensuite la méthode dans cette classe à coté des données. Autre solution, utilise extract méthod pour séparer la méthode en plusieurs parties qui pourront être placée chacune dans une classe différente.

## Résultat

- Moins de duplication de core
- Meilleur organisation du code
