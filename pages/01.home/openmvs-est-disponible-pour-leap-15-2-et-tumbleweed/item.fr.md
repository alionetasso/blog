---
title: 'openMVS est disponible pour Leap 15.2 et Tumbleweed'
media_order: chateau_de_sceaux.png
published: false
feed:
    limit: 10
---

Depuis quelques semaines, le paquet [openMVS](https://cdcseacave.github.io/openMVS/) est disponible dans le dépôt _graphics_. Il est le complément quasi-indispensable à [openMVG](http://imagine.enpc.fr/~moulonp/openMVG/) pour finaliser un modèle 3D quand on se entreprend un traitement d'images par corrélation dense. Ce traitement d'images fait partie d'un sujet plus vaste qu'on nomme "Photogrammétrie". Par abus de langage on peut parfois confondre les deux, alors laissons de côté pour l'instant le terme "Photogrammétrie" et étudions simplement le traitement d'images par corrélation dense.

* Présentation d'openMVS et de ses outils

Le paquet openMVS propose 7 outils : 4 pour traiter les données, 2 pour convertir les objets, et 1 pour visualiser les résultats (intermédiaires ou finaux). On retiendra donc **DensifyPointCloud**, **ReconstructMesh**, **RefineMesh** et **TextureMesh** pour traiter les données produites en amont par openMVG.

* Le principe de _pipeline_ : exemple et résultat

openMVG et openMVS s'utilisent en ligne de commande, pas d'interface graphique autre que le **Viewer** d'openMVS. Voyons donc sur un schéma comment tout cela s'articule, quand on compare à d'autres processus de traitement tels que [MVE](https://www.gcc.tu-darmstadt.de/home/proj/mve/) et [VisualSFM](http://ccwu.me/vsfm/) :

[![SfM_Pipeline](http://epysod12.free.fr/Alionet/openMVS/SfM_Pipeline.png){width=60%}](http://epysod12.free.fr/Alionet/openMVS/SfM_Pipeline.png)

Et voici un exemple en images avec d'un côté les photos de départ d'un sujet de type architectural, et de l'autre un rendu intermédiaire, ouvert dans MeshLab :

![](http://imagine.enpc.fr/~moulonp/openMVG/SfM_Images/input_images.jpg){width=40%}
![](http://imagine.enpc.fr/~moulonp/openMVG/SfM_Images/dense_Front.jpg){width=30%}
