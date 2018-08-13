# Refused Request

## Symptomes

Lorsqu'une classe fille qui utilise uniquement certaines méthodes et propriétés héritées de sa classe mère, la hiérarchie est suspecte. Les méthodes non necessaires pourraient devenir inutiles ou être redéfinies pour supprimer les exceptions.

## L'origine du problème

Un développeur a utiliser l'héritage pour faire de la réutilisation du code de la classe mère. Mais la super-classe et la sous-classe sont totalement différentes.

## Correction

L'héritage n'a aucun sens et la sous-classe n'a rien en commun avec la superclasse. Eliminer l'héritage en faveur de la composition avec : __Replace Inheritance with delegation__.

Si l'héritage est approprié, débarassez-vous des champs et méthodes non necessaires. Extraire de la super-classe tous les champs et méthodes utilisés par la sous-classe, les mettre dans une nouvelle classe et faire hériter les deux classes de cette nouvelle classe.

## Résultat

Améliore la lisibilité et l'organisation du code. Supprime les dépendances étranges.

