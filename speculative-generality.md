# Généralisation spéculative

## Symptomes

une classe, méthode, champs ou paramètre inutilisé.

## L'origine du problème

Parfois le code est écrit "juste au cas où". De futures évolutions sont ainsi anticipées. Cependant il n'est pas rare que ces évolutions ne soit jamais implémentées. On obtient alors du code difficile à comprendre et maintenir car trop compliqué.

## Correction

Pour supprimer des classes abstraites inutilisées, essayer __Collapse Hierarchy__.

- Eliminer les delegations à une autre classe inutiles avec __Inline Class__.
- Supprimer les methodes inutiles avec __Inline Method__.
- Les méthodes avec des paramètres inutilisés doivent être traitées avec __Remove parameter__
- Les propriétés inutilisées doivent être supprimées.

## Résultat

- Code plus concis
- Maintenance facilitée

## Quand ignorer

- Dans un framework il est raisonnable de créer des fonctions inutilisés dans le framework lui-même. Tant qu'elles sont utilisées par les clients.
- Avant de supprimer un élement, s'assurer qu'ils ne sont pas utilisés dans des tests unitaires. Cela peut arriver quand le test a besoin d'informations interne à la classe.
