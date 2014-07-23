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

- Nous allons faire un texte à l'intérieur d'un cercle pour notre exemple. La particularité est qu'il ne s'agit pas par défaut d'un chemin exploitable. Il va falloir convertir en chemin vectoriel la police de caractère pour que la CNC puisse travailler correctement. Pour ce faire, sélectionner vos objets, puis dans le menu, **Chemin > Objet en chemin**. Votre police de caractère est ainsi converti. Même chose pour le cercle si vous voulez transformer les contours en deux traits: **Chemin > Contour en chemin**

- Une fois votre objet converti, nous allons utiliser une extension qui permet de générer automagiquement le fichier nécessaire à la suite de notre exemple.
- La première étape est déjà faite, il suffit de fixer notre objet sur le calque 1. Utilisez le petit cadenas en bas à gauche pour ce faire. Vous protégerez ainsi votre premier calque de toutes modifications.
- Ensuite, nous allons créer un second calque: **Calque > Ajouter un calque** ou **MAJ + CTRL + N**. Vous pouvez le nommer comme bon vous semble, nous l'appellerons "gcode" dans notre cas.
- Pour créer le fichier, rendez-vous dans l'onglet **Extensions > GCode Tools > Orientation Points**.
  - choisir 2 points mode
  - **Z surface** correspond à l'origine, **Z depth** à la profondeur. Cela correspond au déplacement vertical de la fraise. Plus vous voudrez attaquer le matériau en profondeur, plus votre **Z Depth** sera important.
  - **Units** en mm
  - **Appliquer** puis **Fermer**

- Ensuite, **Extensions > GCode Tools > Tools Library**. Ici, on va selectionner quel type d'outil nous allons utiliser. Vous pourrez en effet utiliser différent type de fraise selon votre matériau. Nous utiliserons dans notre exemple l'outil "cone" puis **Appliquer** et **Fermer**. Sur votre calque apparaît  alors un cadre contenant des paramètres générés automatiquement. Ce calque ne sera pas gravé, seul le premier sera pris en compte. Vous pourrez toutefois modifier quelques paramètres de vitesse de rotation ou de diamètre de fraise par exemple.

- Enfin, **Extensions > GCode Tools > Path to Gcode**. Dans l'onglet "preferences", nommez le fichier qui sera généré, ainsi que son destination finale dans vos répertoires. Sélectionner pour finir le premier onglet "Path to G Code" avant d'**Appliquer** et **Fermer**. Votre fichier .gnc est prêt. Vous remarquerez les petites flèches apparaissant sur votre projet. Elles illustrent le déplacement de la tête de fraisage.

## Mettre en route la machine
- L'interrupteur se trouve sur la gauche du châssis.
- Brancher l'usb sur le pc. Vous devriez voir apparaître sur votre bureau un nouveau périphérique, nommé "MyLinuxLive" dans notre cas, et contenant les fichiers de configuration de la carte électronique.
- Installer puis lancer le logiciel CuteCom : [CuteCom](http://cutecom.sourceforge.net/)
CuteCom est un petit logiciel (API???) qui sert de transfert entre le .ngc créé par Inkscape et la CNC
    - Commencer par choisir le **Device** c'est la liaison série entre votre CNC et le PC.
Ce doit être /dev/ttyACM0. Le Baud rate doit être à : 9600
    - Ensuite vous cliquez sur Open device en haut à gauche, et c'est tout.
- Tester le fonctionnement en écrivant dans la fenêtre input en bas **M3** (cela devrait mettre en route votre moteur) Puis taper **M5** pour l'éteindre.

## Lancer la gravure

## Changer les outils
Il vous faut 2 clés plates : 10 et 13 mm.
Maintenir le [mandrin](http://fr.wikipedia.org/wiki/Mandrin) avec la clé de 13 et avec la clé de 10 vous tournez dans le sens horaire pour desserrer et antihoraire pour serrer.
Vous ôtez l'écrou qui sert l'outil dans le mandrin.
Puis vous changez votre outil.
La queue des outils utilisable avec le mandrin sur la CNC sont de diamètre 3.17 mm

## Mettre en place sa plaque
Il vous faut 2 tailles de clé 6 Pans mâle (Allen) : du 4 et du 5 mm
Les 2 vis de serrage servent à déplacer les mords de blocage de votre pièce, vous allez faire le blocage grossièrement.
La vis 6 pans de 5 mm vous sert pour le maintien fin.




# Todo

- Ajouter au chassie un bouton d'arrêt d'urgence sur l'USB.
- Faire une sauvegarde des fichiers configuration qui fonctionnent du firmware smoothieboard.
- Réaliser un blocage en Z car **NOTRE** machine a tendance à avoir le moteur qui descend tout seul avec les vibrations, et du coup cela creuse plus que prévue dans votre matière.
- Agrandir la fenêtre (à droite de la machine) permettant de régler manuellement le déplacement sur X
- Matérialiser visuellement les 3 axes : X, Y, Z


