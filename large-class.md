# Grande classe

## Symptomes

Une classe qui contient beaucoup de : 
- champs
- méthodes
- lignes de code

## L'origin du problème

La plupart des classes naissent petites. Mais elles grossissent au fur et à mesure des évolutions.

Ceci est dû, comme pour les longues méthodes, au fait que les programmeurs trouve généralement plus facile d'ajouter le code dans une classe existante que de créer une nouvelle classe.

## Correction

La classe a trop d'usages, il faut essayer de les regrouper pour les séparer :
- L'__extraction de classe__ va aider si une partie des fonctionnalités de la grande classe peut être transférée vers un autre composant.
- L'__extraction de classe fille__ aide si une partie du comportement peut être fait de plusieurs manière ou si du code est appelé rarement.
- L'__extraction d'interface__ aidera s'il est necessaire d'avoir une liste de comportement à présenter aux clients de la classe.
- Si la grande classe est responssable de composants d'interface, il est possible de transférer certaines données et comportements dans une classe métier. 

## Résultat

- Refactorer la grande classe évite aux développeurs de devoir se rappeler un grand nombre d'attributs pour une classe.
- Dans de nombreux cas, découper une grande classe évite la duplication de code et de fonctionnalités.
