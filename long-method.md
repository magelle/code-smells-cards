# Long Method

## Symptomes

Une méthode contenant trop de lignes de code. En générale, une méthode de plus de 10 lignes devrait vous interpeler.

## L'origine du problème

Après sa création, la méthode a continuer à recevoir de nouvelles choses sans que rien ne lui soit jamais retiré. Puisqu'il est plus facile d'écrire du nouveau code que de lire de l'ancien, ce smell reste non visible jusqu'à ce que la méthode se transforme en paquet de code incompréhensible.

Il est souvent plus facile de modifier une méthode existante que d'en créer une nouvelle. "Juste deux lignes de plus, pas besoin de créer une nouvelle méthode" Ainsi un peu de code est ajouté à la méthode existante, puis un peu plus, puis un peu plus ...

## Correction

Lorsque vous souhaitez écrire un commentaire pour expliquer un bloc de code ou lorsque vous séparez des blocs de code entre aux, c'est le signe que vous devriez créer une nouvelle méthode.
Même une ligne seule devrait être extraite dans une méthode séparée si elle requière une explication.
Si la nouvelle méthode a un nom explicite, il n'y aura aucun besoin d'aller en voir le contenu pour savoir ce qu'elle fait.

- Pour réduire la taille d'une méthode, utiliser __Extract Method__
- Si des variables locales ou des paramètres vous en empêche, utiliser __Replace Temp with Query__, __Introduce Parameter Object__ ou __Preserve Whole Object__
- Si les méthodes précédentes ne vous aident pas essayer __Replace Method with Method Object__
- Les if et les boucles sont de bons inndices du code qui peut être extrait. Vous pouvez utiliser __Decomlpose conditional__

## Résultat

- Dans la programmation orienté objet, les classes avec de petites méthodes vivent plus longtemps.
- Plus une méthode est longue, plus est est compliquée à comprendre et à maintenir.
- Les longue méthode sont des cachettes parfaites pour les bugs et le code dupliqué

## Performance

Beaucoup arguent que créer des méthodes impact la performance. Cependant cet impact est si négligeable que cela ne vaut pas la peine de s'en inquiéter.

De plus le code lisible et maintenable rend la découverte des problèmes de performances et la restructuration plus facile.

