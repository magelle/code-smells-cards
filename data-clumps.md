# Data Clumps

## Symptomes

Différentes parties de code qui contienent les même amas de données (ex: informations de connexion à la base de données). Ces amas devraient être transformés en une classe spécifique.

## L'origine du problème

Ces amas de données sont souvent du à des copier-collers mal venus.

Pour savoir si des données forment un amas, supprimer une partie des données pour voir si le reste des données reste cohérent. Si ce n'est pas le cas, les données devrait être regroupées au sein d'un même objet.

## Correction

- Si un amat est composés d'attributs de classe, utiliser __Extract Class__ pour les transférer vers leur propre classe.
- Si l'amas de données est utiliser dans les paramètres de méthodes, utiliser __Introduce Parameter Object__
- Si certaines données sont passées à d'autres méthodes il est possible de l'objet entier en paramètre. __Preserve Whole Object__ vous aidera à faire ça.
- Regarder le code utilisant ces données, une partie de ce code pourrait être déplacé vers la classe de données.

## Résultat

- Améliore la lisibilité du code et son organisation. Les opérations sur ces données particulière sont regroupées au sein d'un seul objet au lieu d'être dispersées dans la base de code.
- Réduit la taille du code

## Quand ignorer

Passer un objet en paramètre au lieu de variables de type primitifs peut créer un dépendance indésirable entre deux classes.

