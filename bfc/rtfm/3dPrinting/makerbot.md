##Suivi des imprimantes du Lab

###REPLI 2X 01 (En service)

###FAQ

####Installer (ré-installer) les drivers d'une makerbot

Retour d'expérience de Raphaël Foisy-Marquis, animateur multimédia à la MQ Villejean:

"Lors de l'installation de l'imprimante 3D, la Replicator 2X, la liaison entre le logiciel Makerware et la machine ne se faisait pas.
Les pilotes ne voulaient pas s'installer.
J'ai donc envoyé une requête à Makerbot qui m'ont envoyé cette démarche à suivre. (le PC est sous Windows XP)

- Assurez-vous que l'imprimante est branché à un port USB. 
- Accédez au Propriété système (dans le menu démarrer clic droit sur Poste de travail, puis Propriété), Passez à l'onglet Matériel, puis sur "Gestionnaire de périphériques" pour ouvrir le Gestionnaire de périphériques. Un appareil avec un point d'interrogation jaune appelé "The Replicator" devrait apparaître sous d'autres périphériques. 
- Cliquez-droit sur "The Replicator", puis choisissez Mettre à jour le pilote. Cela devrait ouvrir l'Assistant de mise à jour du matériel. 
- Choisissez "Non, pas pour cette fois", puis appuyez sur "Suivant>". 
- Choisissez "Installer à partir d'une liste ou d'un emplacement spécifié (Avancé)", puis appuyez sur "Suivant>". 
- Décochez la case «Rechercher dans les médias amovibles (disquette, CD-ROM ...)», sélectionnez «Inclure cet emplacement dans la recherche:", puis appuyez sur "Parcourir". Cela devrait ouvrir la boîte de dialogue Rechercher un dossier. 
- Choisissez dans "C: \ Program Files \ MakerBot \ drivers", puis appuyez sur "Ok". Appuyez sur "Suivant>". 
- Appuyez sur "Terminer" pour terminer le processus d'installation du pilote.

Et ça a marché.
Car je n'avais pas installé le logiciel dans C:\ Programme Files, ce qui explique la non installation des drivers. Et donc j'ai spécifié l'emplacement des dossiers du logiciel.

Ce qu'il y a de bon à retenir, c'est que les drivers sont inclus dans l'installation du logiciel."

####Démontage des têtes d'impression:

En cas d'impression ratée qui aurait fondue sur les têtes un démontage peut être nécessaire, voici comment procéder: 

Débrancher le moteur d'extrusion

 ![moteur débranché](https://farm4.staticflickr.com/3813/13305203954_321da98c0e.jpg "Débrancher le moteur d'une tête d'extrusion replicator")

Dévisser les vis mécaniques qui maintiennent le radiateur et le ventilateur sur la tête d'impression.

![vis mécaniques dévissées](https://farm3.staticflickr.com/2827/13305200564_a69af0f9b1.jpg "Dévisser les vis mécaniques")

Retirer le bloc de refroidissement et le moteur d'xtrusion. Les mettre de côté avec les vis

![refroidissement](https://farm4.staticflickr.com/3815/13305203124_7c68e211a3.jpg "Retirer le bloc de refroidissement")
![moteurext](https://farm3.staticflickr.com/2827/13305206884_ca3b1aaf6d.jpg "Retirer le moteur d'extrusion")

Dévisser le chassis de support des têtes d'impression

![Chassis](https://farm8.staticflickr.com/7352/13304992093_09650656e8.jpg "Retirer le chassis")

Dévisser la vis qui maintient la tête d'extrusion encrassée sur le chassis

![Tête](https://farm3.staticflickr.com/2852/13304848255_d625122c56.jpg "Libération de la tête")

Nettoyer la tête en prenant bien garde à ne pas heurter les blocs de céramique qui entourent la tête et assurent la constance des températures. 

![Nettoyage tête](https://farm8.staticflickr.com/7363/13304839415_4d68578430.jpg "nettoyage de la tête")
![Nettoyage tête2](https://farm4.staticflickr.com/3802/13305197264_b8e37246d1.jpg "nettoyage de la tête2")
##Températures de fusions des plastiques 

- ABS noir de marque ultimaker: Plateau 120°C / Tête 240°C