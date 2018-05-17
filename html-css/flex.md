# La Puissance du Flex

Les flexbox permettent de redimensionner dynamiquement des blocs en utilisant uniquement du CSS.
Elles sont très utiles pour créer un layout en toute simplicité.

Pour les exemples suivants, on va partir du code de base que vous pouvez trouver sur ce lien: [Cliquez ici](https://codepen.io/romainvandevoorde/pen/jxeZBp)

Après chaque explication, un lien Codepen vous permettra d'accéder rapidement au résultat si vous le désirez.

## display: flex

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

Testons quelque chose de plus intéressant...

## Proportions

*A ce stade, votre code devrait ressembler à [ceci](https://codepen.io/romainvandevoorde/pen/jxeRPr)*

Au lieu d'attribuer ``flex: 1;`` à tous les éléments, appliquez le à un seul des éléments (via les classes bg1, bg2 ou bg3).

Vous remarquerez que l'élément auquel vous attribuez ce flex devient énorme, alors que les autres sont "écrasés".
Logique ! Cet élément a reçu l'instruction de s'étendre le plus possible, mais les autres non.

Maintenant, ajoutez ``flex: 1;`` à un autre élément.
Maintenant que deux éléments ont reçu l'instruction de s'étendre, ils vont se partager équitablement l'espace libre, et feront tous les deux la même largeur.

[Codepen](https://codepen.io/romainvandevoorde/pen/yjRKMN)

L'équité c'est bien sympa... Mais moi j'aime bien le bleu, alors je voudrais que l'élément 1 prenne la moitié de la place, et que les deux autres se partagent le reste.

Facile ! Il suffit d'indiquer ``flex: 2`` pour bg1 et ``flex: 1`` pour les deux autres éléments.

La propriété ``flex`` permet effectivement d'indiquer à quel point un bloc peut "grossir". Un bloc en ``flex: 2`` prendra tout simplement deux fois plus de place qu'un bloc en ``flex: 1``.

[Codepen](https://codepen.io/romainvandevoorde/pen/odaOZJ)

## Conclusion

J'ai essayé d'introduire dans ce guide l'utilisation basique de flex de façon très pratique et un peu ludique.
**Il ne présente pas toutes les possibilités que flexbox offre.**

Le meilleur moyen pour vous de bien comprendre comment ça fonctionne, c'est d'expérimenter dans Codepen.
C'est valable pour tous les principes du CSS.
Allez dans Codepen, créez des blocs avec des bordures et des backgrounds colorés et expérimentez !

## Liens utiles

[Css-Tricks - A complete guide to flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
[Tuto en français sur le MDN](https://developer.mozilla.org/fr/docs/Web/CSS/Disposition_flexbox_CSS/Concepts_de_base_flexbox)
