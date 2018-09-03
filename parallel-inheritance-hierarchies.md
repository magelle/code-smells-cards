# Parallel inheritance hierarchies

## Symptomes

Lors de la création d'une sous-classe, vous devez créer une sous-classe d'une autre classe.

## L'origine du problème

Tout va bien tant que la hiérarchie reste petite. Mais avec les ajouts de classes, la modifications deviennent de plus en plus difficiles.

## Correction

Vous pouvez dé-dupliquer cette hiérarchie de classe en deux étapes. Premièrement ajouter une référence de la des intances d'une hierarchie dans les classes de l'autre. Ensuite supprimer la seconde hiérarchie en utilisant __Move Method__ et __Move Field__.

## Résultat

- Réduit la duplication

## Quand ignorer

Parfois avoir des hiérarchies paralèlles est une manière d'éviter d'autres problèmes d'architecture.
