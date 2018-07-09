# Primitive Obsession

## Symptomes

- Utiliser des types primitifs au lieu de petits objets pour de simple concepts (Comme les devises, unités de mesures, numéro de téléphone, ...)
- Utiliser une constante pour représenter une information (Comme ADMIN_ROLE = 1 pour exprimer des droits d'administration)
- Utiliser des constants comme nom de propriété pour utilisation dans un tableau de données

## L'origine du problème

L'ajout d'un champs est plus facile que de créer une nouvelle classe. On en ajoute donc un, puis un autre, puis un autre, ...
Rapidement, la classe devient énorme et peu maintenable.

Les primitives sont souvent utilisés à la place d'un type. Alors, au lieu d'une classe, on se retrouve avec un ensemble de nombres ou chaines de caractères qui ont une list de valeurs authorisées.
Des noms facile à comprendre sont données à ces valeurs à travers des constantes qui sont rapidement propagés.

## Correction

Si une classe contient de nombreuses propriétés de type primitif, il doit être possible de les regrouper de manière logique et de leur créer leur propre classe. Mieux, le comportement associé à ces données peut être déplacé vers cette nouvelle class. Pour cela essayer __Replace Data Value with Object__.

- Si les champs de type primitifs sont utilisés en paramètre de méthodes, utiliser __Introduce Parameter Object__ ou __Preserve Whole Object__.
- Quand des données complexes sonty codés dans des variables, utiliser __ Replace Type Code with Class__, __Replace Type Code with Subclasses__ ou __Repllace Type Code with State/Strategy__.
- S'il y a des tableaux parmi les propriétés, utiliser __replace array with Object__.

## Résultat

- Le code devient plus flexible grâce aux objets
- Meilleur lisibilité et organisation du code. Les données et les comportements associés sont au même endroits au lieu d'être dispersés.
- Le code dupliqué devient plus visible.
