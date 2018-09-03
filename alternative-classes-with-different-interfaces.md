# Alternative classes with different interfaces

## Symptomes

Deux classes qui ont les mêmes méthodes sous des noms différents.

## L'origine du problème

Le développeur qui a créer la deuxième ne connaissait probablement pas la première.

## Correction

Essayer de créer une interface commune.

- __Rename method__ pour les rendres identiques dans toutes les classes.
- __Move Method__, __Add parameter__ et __Parametrized Method__ pour rendre la signature et l'implementation identique.
- Si une partie uniquement est dupliquée, essayer __Extract superclass__. Les classes existantes deviendront des classes filles.
- Après avoir refactorer, l'une des classes pourrait être supprimable.

## Résultat

- Supression du code dupliqué.
- Réutilisation accrue.
- Code plus lisible et maintenable.

## Quand ignorer

Parfois fusionner des classes est impossible, trop difficile ou sans interêt. Par exemple lorsque les deux classes sont dans des bibliothèques et que chacune possède sa propre version de la classe.
