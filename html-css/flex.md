# La Puissance du Flex

Les flexbox permettent de redimensionner dynamiquement des blocs en utilisant uniquement du CSS. 
Elles sont très utiles pour créer un layout en toute simplicité. 

Pour les exemples suivants, on va partir du code de base que vous pouvez trouver sur ce lien: [Cliquez ici](https://codepen.io/romainvandevoorde/pen/jxeZBp)

Après chaque explication, un lien Codepen vous permettra d'accéder rapidement au résultat si vous le désirez.

##display: flex

Pour démarrer, il nous suffit d'entrer cette ligne de code dans le CSS du conteneur (``.container``).

    display: flex;
    
Vous pouvez déjà voir que le comportement des éléments enfants (``.element``) a changé: ils se trouvent tous sur une même ligne et prennent toute la hauteur du conteneur.

[Codepen](https://codepen.io/romainvandevoorde/pen/degdJp)

## Une belle colonne ?

Disons que vous voulez créer un menu vertical. Il suffit d'ajouter au CSS du conteneur le code suivant

    flex-direction: column;
    
Et les éléments enfants seront automatiquement agencés en une belle colonne.

Essayez de fixer une hauteur au conteneur, par exemple ``400px``. Vous constaterez que les éléments ne prennent pas toute la hauteur du conteneur. Mais c'est quelque chose qu'il est possible de faire en une ligne de code !

Il suffit d'ajouter cet attribut aux éléments enfants:

    flex: 1;
    
Désormais, chaque élément enfant prend un tiers de la place disponible en hauteur dans leur conteneur.

[Codepen](https://codepen.io/romainvandevoorde/pen/GdYQXO)

## Centrer ?

Flex ne permet pas seulement de prendre toute la place disponible, il permet aussi d'agencer les éléments.
Par exemple, on sait tous à quel point ça peut être casse-tête quand on veut centrer quelque chose verticalement.
Voyons comment le faire en trois lignes de code avec flex.

Enlevez le ``flex: 1;`` des éléments enfants et ajoutez le code suivant au CSS du conteneur:

    justify-content: center;
    
BOUM ! C'est centré verticalement.

*Drops mike*

[Codepen](https://codepen.io/romainvandevoorde/pen/KRGQGE)

## Et maintenant une belle rangée

Si vous effacez le ``flex-direction: column;`` du conteneur, ou que vous remplacez ``column`` par ``row``, le flex passera en mode rangée.

Comme avec les colonnes, vous pouvez centrer le contenu ou lui faire prendre toute la place disponible.