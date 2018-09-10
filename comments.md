# Comments

## Symptomes

Une méthode remplie de commentaires explicatifs

## L'origine du problème

Les commentaires sont souvent écris avec de bonnes intentions quand l'auteur réalise que sont code n'est pas intuitif. Dans ce cas, les commentaires tentent de masquer la perfectibilité du code.

> Le meilleur commentaire est un bon nom de méthode ou classe.

Si vous pensez qu'un morceau de code ne peut être compris sans commentaire, essayé de changer la structure du code afin de rendre ce commentaire inutile.

## Correction

- Si un commentaire explicite une expression complexe, cette expression peut être extraite avec __Extract variable__.
- Si un commentaire explicite une section de code, cette section peut extraite dans sa propre méthode avec __Extract Method__. 
- Si une méthode a déjà été extraite mais que les commentaires sont toujours nécessaire, utiliser __Rename Method__ pour lui donner un nom explicite.
- Si une vérification de l'état est nécessaire pour que le système fonctionne, utiliser __Introduce Assertion__

## Résultat

Le code devient plus simple et intuitif.

## Quand ignorer

Certains commentaires sont utiles :
- Lorsqu'il explique __pourquoi__ le code a cette structure.
- Lorsqu'il explique un algorithme complexe (lorsque toute autre méthode de simplification a échouée).
