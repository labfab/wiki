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
- éventuellement le logiciel "Pronterface", pour celles et ceux qui voudraient une alternative de choix, ou s'engager plus à fond dans le paramétrage de la machine. Il ne sera pas nécessaire à vos premières gravures.
- des matériaux (bois, métaux, acrylique, vinyl, PVC, etc.)

## Warning !

- la fraiseuse est un outil tranchant en rotation. Attention aux bracelets, écharpes, cheveux longs, etc., lorsque la machine est en fonction.

- En cas de souci, pour arrêter le déplacement de la tête en urgence, **ne coupez pas l'alimentation électrique. 
Il suffit simplement de déconnecter le câble USB**.


## Préparer son fichier source



## Mettre en route la machine

## Lancer la gravure



# Todo

- Ajouter au chassie un bouton d'arrêt d'urgence sur l'USB.




