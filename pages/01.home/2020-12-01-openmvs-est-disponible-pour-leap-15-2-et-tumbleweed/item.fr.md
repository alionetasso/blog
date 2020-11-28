---
title: 'openMVS est disponible pour Leap 15.2 et Tumbleweed'
media_order: chateau_de_sceaux.png
published: false
feed:
    limit: 10
---

Depuis quelques semaines, le paquet [openMVS](https://cdcseacave.github.io/openMVS/) est disponible dans le dépôt _graphics_. Il est le complément quasi-indispensable à [openMVG](http://imagine.enpc.fr/~moulonp/openMVG/) pour finaliser un modèle 3D quand on entreprend un traitement d'images par corrélation dense. Ce traitement d'images fait partie d'un sujet plus vaste qu'on nomme "Photogrammétrie". Par abus de langage on peut parfois confondre les deux, alors laissons de côté pour l'instant le terme "Photogrammétrie" et étudions simplement le traitement d'images par corrélation dense.

* Présentation d'openMVS et de ses outils

Le paquet openMVS propose 7 outils : 4 pour traiter les données, 2 pour convertir les objets, et 1 pour visualiser les résultats (intermédiaires ou finaux). On retiendra donc **DensifyPointCloud**, **ReconstructMesh**, **RefineMesh** et **TextureMesh** pour traiter les données produites en amont par openMVG. Chaque outil dispose de ses propres options, pour en prendre connaissance on lance alors le programme sans argument, dans un terminal.

* Le principe de _pipeline_ : exemple et résultat

D'une manière générale, on distingue 4 étapes successives dans l'élaboration d'un modèle 3D, quels que soient les _softs_ utilisés :

1. Alignement des photos
2. Densification du nuage de points
3. Génération du maillage
4. Texturage du maillage d'après les photos

Voyons sur un schéma comment tout cela s'articule, quand on compare à d'autres processus tels que ceux proposés par [MVE](https://www.gcc.tu-darmstadt.de/home/proj/mve/) et [VisualSFM](http://ccwu.me/vsfm/) :

[![SfM_Pipeline](SfM_Pipeline.png?resize=40%)](SfM_Pipeline.png)

Et voici un exemple en images avec d'un côté les photos de départ d'un sujet de type architectural, et de l'autre un rendu (intermédiaire) ouvert dans MeshLab :

![MVG_input_images](MVG_input_images.jpg?resize=80%)
![MVG_output_castle](MVG_output_castle.jpg?resize=40%)

openMVG et openMVS s'utilisent en ligne de commande, pas d'interface graphique autre que le **Viewer** d'openMVS (exemple de rendu dans la première image de l'article). Alors pour traiter un sujet, l'idéal est de scripter l'ensemble du processus, avec parfois des options spécifiques à indiquer. Voici un exemple de _script_ qui met l'accent sur la gestion des _logs_, c'est un moyen efficace pour suivre le processus de traitement des images :

[_RUN_openMVG.sh](http://epysod12.free.fr/Alionet/openMVS/_RUN_openMVG.sh)
(dans cet exemple, le fichier <u>sensor_width_camera_database.txt</u> se situe dans le _home_ utilisateur)

Et enfin, pour mieux comprendre les mécanismes de base, consultez la documentation ici : [openmvg.readthedocs.io](https://openmvg.readthedocs.io/en/latest/)
