# Emmet

Emmet est un outil qui permet de taper son code HTML plus rapidement, sans s'inquiéter de l'indentation et sans risquer de faire des erreurs.

Pour commencer, je vous suggère d'utiliser [Codepen](https://codepen.io/pen) pour expérimenter avec Emmet:
leur éditeur HTML permet par défaut d'utiliser Emmet.

Le [site officiel](https://docs.emmet.io/) d'Emmet propose un [cheat sheet complet](https://docs.emmet.io/cheat-sheet/).
Je rédige celui-ci comme petite introduction, et pour vous éviter une surcharge d'informations.

Allez, on passe à l'action !

## Utilisation de base

Tapez ``div`` et appuyez sur TAB. Vous devriez obtenir:
```
<div></div>
```

Voilà. C'est comme ça que fonctionne Emmet. Vous écrivez ce que vous voulez, vous appuyez sur TAB, il crée vos balises.

## Classes et IDs

Tapez ``div.banana``, vous obtiendrez:
```
<div class="banana"></div>
```
Tapez ``div#apple``, vous obtiendrez:
```
<div id="apple"></div>
```
Concrètement, si vous tapez uniquement une classe ou un id, par défaut Emmet créera un ``div``.

Tapez ``.carrot``, vous obtiendrez:
```
<div class="carrot"></div>
```
## Enfants

Tapez ``div>p``, vous obtiendrez:
```
    <div>
      <p></p>
    </div>
```
Tapez ``section>div>a``, vous obtiendrez:
```
    <section>
      <div><a href=""></a></div>
    </section>
```
## Multiplicateurs

Tapez ``header>nav>a*5``, vous obtiendrez
```
    <header>
      <nav>
        <a href=""></a>
        <a href=""></a>
        <a href=""></a>
        <a href=""></a>
        <a href=""></a>
      </nav>
    </header>
```
Tapez ``section>div*2>a*3``, vous obtiendrez:
```
    <section>
      <div>
        <a href=""></a>
        <a href=""></a>
        <a href=""></a>
      </div>
      <div>
        <a href=""></a>
        <a href=""></a>
        <a href=""></a>
      </div>
    </section>
```
## Frères

Tapez ``article>h2+p``, vous obtiendrez:

```    
    <article>
      <h2></h2>
      <p></p>
    </article>
```

## Contenu

Tapez ``article>(h2>{Hello World})+p>lorem10``, vous obtiendrez:
```
    <article>
      <h2>Hello World</h2>
      <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Esse, ab.</p>
    </article>
```
``lorem`` suivi d'un nombre *x* génère *x* mots de [Lorem Ipsum](https://fr.wikipedia.org/wiki/Faux-texte).

# Conclusion

Emmet offre beaucoup d'autres possibilités, ainsi qu'un système similaire pour générer du CSS. Pour plus d'informations, consultez la [documentation officielle](https://docs.emmet.io/).

Bon coding !
