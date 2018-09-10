# Lazy Class

## Symptomes

Comprendre et maintenir des classes coûte du temps et de l'argent. Si une classe n'en fait pas assez pour gagner votre attention, elle devrait être supprimée.

## L'origine du problème

La classe est peut-être  devenue ridiculement petite après plusieurs refactoring.
Ou a été créée en anticipation de futures développements qui n'ont jamais été fait.

## Correction

- Les composants *presque* inutiles doivent recevoir le traitement __Inline Method__.
- Pour les sous-classes, essayer __Collapse Hierarchy__.

## Résultat

- Réduit la taille du code.
- Maintenance facilitée.

