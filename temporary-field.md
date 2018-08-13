# Temporary Field

## Symptomes

Un champs temporaire possède une valeur uniquement dans certains cas. Sinon il est vide.

## L'origine du problème

La plupart du temps un champs temporaire est créer lors de l'écriture d'un algorithme qui requière un grand nombre de paramètres. Il est alors plus aisé de créer des champs dans la classe que des paramètres de méthode. Ces champs sont utilisés uniquement dans l'algorithme et donc inutile le reste du temps.

## Correction

- Les champs temporaires et tout le code les utilisant peut être mis dans une classe séparée grâce à __Extract class__. On crée alors un objet méthode de la même manière qu'on le ferait alors avec __Replace Method with object method__.

- Utiliser __Introduce Null Object__ et remplacer le code qui vérifiait la présence des champs temporaire.

## Résultat

Meilleur lisibilité et organisation du code.
