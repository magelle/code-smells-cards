# Shotgun surgery

## Symptomes

Une modification qui necessite de nombreux changements dans de nombreuses classes.

## L'origine du problème

Une responsabilité a été dispersée dans une grand nombre de classes. 

## Correction

Utiliser __Move Method__ et __Move Field_ pour déplacer le code existant dans une seule classe.
S'il n-y-a pas de classe approrié, en créer une.

## Résultat

- Meilleur organisation du code
- Moins de duplication
- Maintenance plus facile
