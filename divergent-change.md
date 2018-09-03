# Divergent change

## Symptomes

Lorsque vous modifiez une classe, vous vous retrouver à devoir modifier de nombreuses méthodes.

## L'origine du problème

Ces modifications divergeantes sont souvent dûes à une mauvaise structure de programme ou à du "Copypasta programming"

## Correction

- Séparer le comportement de la classe avec __Extract class__.
- Si différentes classes ont le même comportement, vous pourriez vouloir utiliser l'héritage (__ERxtract superclass__, __Extract sous-classe__).

## Résultat

- Améliore l'organisation du code.
- Réduit la dupliciation.
- Simplifie la maintenance.
