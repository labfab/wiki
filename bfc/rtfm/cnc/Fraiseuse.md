# Fraiseuse à commande numérique

# Aperçu
Celle du lab est une machine de marque "Portix", récupérée dans un lycée professionnel et dont nous avons remplacé l'électronique de commande par une carte Open Source Hardware, la [Smoothieboard](http://smoothieware.org/smoothieboard) (la même que l'on retrouve sur certaines imprimantes 3D de type RepRap).


photo de la Portix du Lab

# Usage
Cette machine est destinée à graver ou découper la matière, y compris les métaux (contrairement à la laser du lab). Une "fraise" en rotation vient attaquer le matériau selon le fichier source que vous lui aurez fourni. Le format de fichier en entrée est du .svg converti en **.ngc** pour l'envoyer.

La dimension **maximale** de travail est de **130 x 130 mm**.

Pour l'utiliser, il vous faudra, en fonction de vos besoins:
- un logiciel de dessin vectoriel, du type **Inkscape**, qui permettra de modeliser en 2D votre projet.
- le logiciel **Cutecom**, qui sert à convertir le fichier .ngc obtenu auparavant via Inkscape, en fichier gcode, format qu’interprète la machine.
- une fraise adaptée à votre projet. Graver du métal ou du bois ne nécessite pas le même type de fraise.
- des matériaux (bois, métaux, acrylique, vinyl, PVC, etc.)
- éventuellement le logiciel "Pronterface", pour celles et ceux qui voudraient une alternative de choix, ou s'engager plus à fond dans le paramétrage de la machine. Il ne sera pas nécessaire à vos premières gravures.

## Warning !

- la fraiseuse est un outil tranchant en rotation. Attention aux bracelets, écharpes, cheveux longs, etc., lorsque la machine est en fonction.

- En cas de souci, pour arrêter le déplacement de la tête en urgence, **ne coupez pas l'alimentation électrique. 
Il suffit simplement de déconnecter le câble USB**.


## Préparer son fichier source
- Lancer [Inkscape](www.inkscape.org/fr/)
- avant de commencer, nous allons fixer les unités utilisées par défaut avec le raccourci clavier **MAJ + CTRL + D** ou par le menu **Fichier > Propriété du document**. Choisir "mm" si vous voulez travailler en millimètre.

- Nous allons faire un texte à l'intérieur d'un cercle pour notre exemple. La particularité est qu'il ne s'agit pas par défaut d'un chemin exploitable. Il va falloir convertir en chemin vectoriel la police de caractère pour que la CNC puisse travailler correctement. Pour ce faire, sélectionner vos objets, puis dans le menu, **Chemin > Objet en chemin**. Votre police de caractère est ainsi converti. Même chose pour le cercle si vous voulez transformer les contours en deux traits: **Chemin > Contours en chemin**.



## Mettre en route la machine

## Lancer la gravure



# Todo

- Ajouter au chassie un bouton d'arrêt d'urgence sur l'USB.




