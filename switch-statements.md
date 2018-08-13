# Switch Statements

## Symptomes

Un switch ou une séquence de if complexe.

## L'origine du problème

Une utilisation très rare du swatch case est une spécificité de la programmation orienté objet. La plupart du temps un switch peut être réparti à plusieurs endroits dans le code. Quand une condition est ajouter, il faut revoir tout le code du switch case.

La règle de basse est de penser polymorphisme à chaque fois que vous voyez un switch case.

## Correction

- Pour isoler un switch et le mettre dans une classe adapté, utilise __Extract method__ puis __Move method__.
- Si un switch est basé sur un type code, utiliser __Replace Type Code with subclasses__ ou __Replace type code with State/Strategy__.
- Après avoir créé la structure d'héritage, utiliser __Replace Conditional with polymorphism__.
- Si tous les case du switch appellent la même method avec des paramètres différents, le polymorphisme est superflue. Dans ce cas vous pouvez découpée cette méthode en méthodes plus petites avec __Replace Parameter with explicit Methods__.
- Si une des options est null, utiliser __Introduce Null Object__.

## Résultat

Meilleur organisation du code.

## Quand ignorer

- Quand le switch fait des actions simples, il n'y a pas de raison de modifier le code.
- Dans les design pattern factory, le switch est souvent utilisé pour choisir la classe à créer.

