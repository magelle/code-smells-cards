# Duplicate Code

## Symptomes

Deux frargments de code *presque* identiques.

## L'origine du problème

Le code dupliqué apparait lorsque plusieurs programmeurs travaillent sur différentes parties d'un même programme. Il sont alors inconscients du code écrit par leurs collègues.

Il peut aussi exister des sections de code qui semblent différentes mais qui ont le même comportement.

Parfois la duplication est intentionnelle lorsque, pressés par les délais, un code presque bon est copier-coller.

## Correction

- Si le code se trouve dans plusieurs méthodes, utiliser __Extract Method__ et utiliser la méthode à la place du code dupliqué.
- Si le code duplpiqué est dans deux sous-classes du même niveau :
 - Utiliser __Extract Method__ sur les deux classes puis __Pull Up Field__ pour les champs utilisé par cette méthode.
 - Si le code dupliqué est dans le contructeur, utiliser __Pull Up Constructor Body__.
 - Si le code dupliqué n'est pas complètement identique, utiliser _Form Template Method__
 - Si deux méthodes font la même chose avec deux algorithmes différents, selectionner le meilleur et appliquer __Substitute Algorithm__.
- Si le code dupliqué est dans deux classes différentes,utiliser __Extract Class__ dans une classe et utiliser ce nouveau composant dans l'autre.
- Si un grand nombre d'expressions conditionnelles font exécutent le même code, fusionner ce code en utilisant __Consolidate Conditionnal Expression__ et utiliser __Extract Method__ pour déplacer la condition dans une méthode séparée avec un nom facile à comprendre.
- Si le même code est exécuté dans toutes les branches d'une expression conditionnel, placer le code à l'extérieur des conditions en utilisant __Consolidate Duplicate Conditional Fragments__.

## Résultat

- Fusionner le code dupliqué simplifie la structure du code et le rend plus intelligible.
- Simplification et brièveté rendent le code plus facile à comprendre et à maintenir.

## Quand ignorer

Dans de très rares cas, fusioner deux sections de code identiques rend le code moins lisible.
