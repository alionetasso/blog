---
title: 'openMVS est disponible pour Leap 15.2 et Tumbleweed'
media_order: chateau_de_sceaux.png
published: true
feed:
    limit: 10
---

Depuis quelques semaines, le paquet [openMVS](https://cdcseacave.github.io/openMVS/) est disponible dans le dépôt [graphics](https://download.opensuse.org/repositories/graphics/). Il est le complément quasi-indispensable à [openMVG](http://imagine.enpc.fr/~moulonp/openMVG/) pour finaliser un modèle 3D quand on entreprend un traitement d'images par corrélation dense. Ce traitement d'images fait partie d'un sujet plus vaste qu'on nomme "Photogrammétrie".

Par abus de langage on peut parfois confondre les deux, alors laissons de côté pour l'instant le terme "Photogrammétrie" et étudions simplement le traitement d'images par corrélation dense.

## Présentation d'openMVS et de ses outils

L'installation du paquet openMVS est désormais possible en ajoutant le dépôt _graphics_ au préalable, comme ceci (en _root_) :  
`zypper addrepo https://download.opensuse.org/repositories/graphics/openSUSE_Leap_15.2/graphics.repo`  
ou :  
`zypper addrepo https://download.opensuse.org/repositories/graphics/openSUSE_Tumbleweed/graphics.repo`

puis :  
`zypper refresh`  
`zypper install openMVS`

(note : si openMVG n'est pas installé, alors faites : `zypper install openMVG`)

Le paquet openMVS propose 7 outils : 4 pour traiter les données, 2 pour convertir les objets, et 1 pour visualiser les résultats (intermédiaires ou finaux). On retiendra donc **DensifyPointCloud**, **ReconstructMesh**, **RefineMesh** et **TextureMesh** pour traiter les données produites en amont par openMVG. Chaque outil dispose de ses propres options, pour en prendre connaissance on lance alors le programme sans argument, dans un terminal.

## Le principe de _pipeline_ : exemple et résultat

Le but d'openMVS est de (re)créer une scène en 3 dimensions à partir du jeu de données produit par openMVG. Ce dernier est donc l'étape préliminaire indispensable à toute opération : openMVG analyse les photographies qu'on lui indique et calcule les positions des objectifs et des points "clés" afin de proposer un rendu 3D de l'objet photographié. Car c'est bien ça le point de départ : **les photos !**.

En résumé : si on associe **openMVG + openMVS**, alors on a la combinaison idéale pour générer un modèle 3D texturé en HD, à partir de simples photos (en JPG, sans zoom de préférence), pour autant qu'on respecte certaines règles dans le processus de traitement.

D'une manière générale, on distingue 4 étapes successives dans l'élaboration d'un modèle 3D, quels que soient les _softs_ utilisés :

1. Alignement des photos
1. Densification du nuage de points
1. Génération du maillage
1. Texturage du maillage d'après les photos

Voyons sur un schéma comment tout cela s'articule, quand on compare à d'autres processus tels que ceux proposés par [MVE](https://www.gcc.tu-darmstadt.de/home/proj/mve/) et [VisualSFM](http://ccwu.me/vsfm/) :

[![SfM_Pipeline](SfM_Pipeline.png?resize=40%)](SfM_Pipeline.png)

Et voici un exemple en images avec d'un côté les photos de départ d'un sujet de type architectural, et de l'autre un rendu (intermédiaire) ouvert dans MeshLab :

![MVG_input_images](MVG_input_images.jpg?resize=80%)
![MVG_output_castle](MVG_output_castle.jpg?resize=40%)

openMVG et openMVS s'utilisent en ligne de commande, pas d'interface graphique autre que le **Viewer** d'openMVS (exemple de rendu dans la première image de l'article). Alors pour traiter un sujet, l'idéal est de scripter l'ensemble du processus, avec parfois des options spécifiques à indiquer.

Voici un exemple ici avec **RUN_openMVG_openMVS.sh**, en lien sur cette page : [SfM_Tools](https://gitlab.volted.net/epysod12/sfm_tools)  
Ce _script_ met l'accent sur la gestion des _logs_, c'est un moyen efficace pour suivre le processus de traitement des images.  
(dans cet exemple, le fichier <u>sensor_width_camera_database.txt</u> se situe dans le _home_ utilisateur)

Pour mieux comprendre les mécanismes de base, n'hésitez pas à consulter la documentation ici : [openmvg.readthedocs.io](https://openmvg.readthedocs.io/en/latest/)

Et enfin, rendez-vous sur le forum pour approfondir un peu plus le sujet :
