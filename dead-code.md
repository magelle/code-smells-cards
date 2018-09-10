# Dead code

## Symptomes

Une variable, un paramètre, un champs, une méthode, ou une classe qui n'est plus utilisée.

## L'origine du problème

Alors que le programme évolue, personne n'a pris le temps de nettoyer l'ancien code.

Du code mort peut assi être trouvé dans des structures conditionnelles complexes. Lorsqu'une des branches devient inatteignable.

## Correction

La méthode la plus rapide est de trouver le code mort avec son IDE. Puis de le supprimer.

- Dans le cas d'une classe inutile, __Inline Class__ ou __Collapse Hierarchy__ peuvent être appliqués si la sous-classe ou super-classe est utilisée.
- Pour supprimer un paramètre inutilisé, appliquer __Remove Parameter__.

## Résultat

- Réduit la taille du code.
- Simplifie sa maintenance.
