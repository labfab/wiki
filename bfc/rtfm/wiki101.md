# Question Fréquemment Posées en matière d'utilisation de ce Wiki

Le système de Wiki mis en place pour est basé sur [Gollum](https://github.com/gollum/gollum) et utilise git. La syntaxe utilisée par défaut est le langage de balisage [markdown](http://fr.wikipedia.org/wiki/Markdown), on peut cependant utiliser d'autres langages de balisages utilisés par des moteurs tels que MediaWiki, RDoc ou encore [Textile](http://fr.wikipedia.org/wiki/Textile_(langage))

**Remarque : on utilise très souvent en markdwon les indentations (listes...) qui correspondent à quatres espaces simples (et non une tabulation !)**

## Comment faire un titre, un sous-titre, une liste, un bloc de code ?

### Titres et sous-titres
On utilise le symbole # avant le titre, qui détermine le niveau de titre souhaité (le HTML propose 6 niveaux de titres de `<h1>` à `<h6>`)
Pour un titre de premier niveau on utilisera #, second niveau ## et ainsi de suite

### Listes
#### Liste non ordonnée
    * Premier élément
        * Sous-élément
    * Second élément
    * Troisième élément

On obtiendra donc en markdown

* Premier élément
    * Sous-élément
* Second élément
* Troisième élément

#### Liste ordonnée
    1. Premier élément
        * Premier sous-élément
        * Second sous-élément
    2. Second élément
        1. Premier sous-élément ordonné
        2. Second sous-élément ordonné
    3. Troisième élément

On obtiendra donc en markdown

1. Premier élément
    * Premier sous-élément non ordonné
    * Second sous-élément non ordonné
2. Second élément
    1. Premier sous-élément ordonné
    2. Second sous-élément ordonné
3. Troisième élément

### Code et bloc de code
Pour afficher un bloc de code il suffit simplement de précéder les lignes à afficher par une indentation correspondant donc à quatres espaces :
        Ceci est un bloc
        de code sur plusieurs
        lignes


## C'est quoi ce formalisme ?
_Lien vers [markdown](http://ivfe.auf.org/plateforme/help.php?file=markdown.html), [markdown avancé](http://ivfe.auf.org/plateforme/help.php?file=advanced_markdown.html) et un [éditeur en ligne](http://dillinger.io/) pour s’entraîner.


## Comment faire pour les photos ?
- rapide intro à l'usage du compte flickr Lab pour le stockage des images utilisées en illustration du wiki.
- tuto sur les images liées, locales, distantes, le copyright.

## Comment faire une Table des Matières dans sa page ?

En ajoutant simplement la balise `[[_TOC_] ]`
là où vous désirez la voir apparaître dans votre page. Vous pouvez aussi éditer une page et voir par vous même comment le résultat attendu a été obtenu. TOC correspond à l'acronyme anglais _Table Of Content_