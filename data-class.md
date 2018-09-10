# Data class

## Symptomes

Une classe qui contient uniquement des champs et des méthodes pour y accéder (getters et setters). Ce sont de simples conteneurs de données utilisés par d'autres classes. Ces classes ne contiennent aucun comportement. 

## L'origine du problème

Il est normal qu'une nouvelle classe ne contienne que quelques champs publiques (avec leurs getters et setters) mais la vrai puissance des objets est qu'ils peuvent contenir les données et les traitements qui vont avec.

## Correction

- Si la classe contient des champs public, utiliser __Encapsulate Field__ pour supprimer les accès directs.
- Utiliser __Encapsulate Collection__ pour les données stockées dans des collections.
- Parcourir les clients de cette classe, il est possible de trouver des comportements qui devrait être dans la classe. Utiliser alors __Move Method__ et __Extract Method__.

- Après avoir migré les comportements dans la classe il est de supprimer les anciennes méthodes qui donnent trop d'accès aux données de la classe. Pour cela : _Remove Settings Method__ et __Hide Method__ peuvent être utiles.

## Résultat

- Améliore la cohérence et l'organisation du code. Les opérations sur des données particulière sont maintenant au même endroit au lieu d'être dispersées au hazard.
- Aide à repérer les duplications de code.
