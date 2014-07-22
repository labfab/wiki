# Fraiseuse à commande numérique

Il s'agit d'une machine-outil à commande numérique, de l'anglais **C**omputer **N**umerical **C**ontrol, traduit par [**C**ommande **N**umérique par **C**alculateur](http://fr.wikipedia.org/wiki/Machine-outil_%C3%A0_commande_num%C3%A9rique)

Plusieurs dimensions sont possibles, allant de la petite fraiseuse comme celle présente au lab, jusqu'à la grosse CNC accueillant un panneau de contre-plaqué en entier.

# Aperçu
Celle du lab est une machine de marque "Portix", récupérée dans un lycée professionnel et dont nous avons remplacé l'électronique de commande par une carte Open Source Hardware, la Smoothieboard (la même que l'on retrouve sur certaines imprimantes 3D de type RepRap).

photo de la Portix du Lab

# Usage
Cette machine est destinée à graver ou découper la matière, y compris les métaux (contrairement à la laser du lab). Une "fraise" en rotation vient attaquer le matériau selon le fichier source que vous lui aurez fourni. Le format de fichier en entrée est .ngc

La dimension **maximale** de travail est de **130 x 130 mm**.

Pour l'utiliser, il vous faudra, en fonction de vos besoins:
- un logiciel de dessin vectoriel, du type Inkscape, qui permettra de modeliser en 2D votre projet.
- le logiciel "Cutecom", qui sert à convertir le fichier .ngc obtenu auparavant via Inkscape, en fichier gcode, format qu’interprète la machine.
- éventuellement le logiciel "Pronterface", pour celles et ceux qui voudraient une alternative de choix, ou s'engager plus à fond dans le paramétrage de la machine. Il ne sera pas nécessaire à vos premières gravures.



