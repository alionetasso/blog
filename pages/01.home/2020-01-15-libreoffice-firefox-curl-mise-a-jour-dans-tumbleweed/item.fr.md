---
title: 'LibreOffice, Firefox et Curl reçoivent des mises à jour dans Tumbleweed'
taxonomy:
    category:
        - blog
    tag:
        - tumbleweed
visible: false
feed:
    limit: 10
titre: 2020-01-15-libreoffice-firefox-curl-mise-a-jour-dans-tumbleweed
---


Plusieurs paquets ont été mis à jour cette semaine dans [openSUSE](https://www.opensuse.org/) [Tumbleweed](https://en.opensuse.org/Portal:Tumbleweed) comme prévu après la saison des vacances. Cinq instantanés de cette version évolutive ont été livrés cette dernière semaine après avoir passé les tests rigoureux appliqués par [openQA](http://open.qa/).

Ces versions sont incroyablement stables avec des notes enregistrées au-dessus 95, selon le [Tumbleweed snapshot reviewer](http://review.tumbleweed.boombatower.com/).

L'instantané le plus récent, [20200112](https://lists.opensuse.org/opensuse-factory/2020-01/msg00202.html), a mis à jour [Xfce](https://www.xfce.org/) avec une mise à jour pour xfce4-session 4.14.1 et xfce4-settings 4.14.2.

Divers changements visibles pour les développeurs ont été apportés dans l'instantané 20200101 dont [re2](https://github.com/google/re2) de Google  une [bibliothèque](https://en.wikipedia.org/wiki/Library_(informatique)) pour [expressions régulières ](https://en.wikipedia.org/wiki/Regular_expression).
[frogr](https://wiki.gnome.org/Apps/Frogr), l'application [GNOME](https://www.gnome.org/) pour la gestion des images avec un compte Flickr, a été mis à jour en 1.6 et a supprimé l'usage obsolète de [GTimeVal](https://people.gnome.org/~ryanl/glib-docs/glib-Date-and-Time-Functions.html#GTimeVal). La plate-forme open source pour le [scale-out](https://en.wikipedia.org/wiki/Scale-out) du [stockage cloud](https://en.wikipedia.org/wiki/Cloud_storage ) public et privé, [glusterfs](https://www.gluster.org/) 7.1, a corrigé le rééquilibrage du stockage provoqué par une erreur d'entrée et une fuite de mémoire dans [glusterfsd](https://github.com/gluster/glusterfs/processusblob/master/glusterfsd/src/glusterfsd.c).

La version 7.0.9.14 de [ImageMagick](https://www.imagemagick.org/) a optimisé les performances des effets spéciaux de [Fx](https://imagemagick.org/script/fx.php) et de [virglrenderer](https://gitlab.freedesktop.org/virgl/virglrenderer) 0.8.1, qui est un projet visant à étudier la possibilité de créer un [GPU](https://en.wikipedia.org/wiki/Graphics_processing_unit) 3D virtuel  pour une utilisation à l'intérieur des machines virtuelles [qemu](https://en.wikipedia.org/wiki/QEMU) afin accélérer le rendu 3D.

L'instantané a continué de mettre à jour les paquets pour [KDE](https://kde.org/) [Applications 19.12.1](https://kde.org/announcements/releases/19.12.1/) qui avaient été intégré dans l'instantané [20200111 ](https://lists.opensuse.org/opensuse-factory/2020-01/msg00197.html). Des améliorations ont été apportées à la vitesse de la molette de défilement pour [Dolphin](https://kde.org/applications/system/dolphin/) de KDE et le logiciel de montage vidéo [Kdenlive](https://kdenlive.org/en/) avait plusieurs correctifs et un ajustement pour un rendu plus rapide, du code obsolète a aussi été supprimé du paquet de diagramme des applications [parapluie](https://umbrello.kde.org/). La plupart des paquets [Applications KDE](https://kde.org/applications/) ont également mis à jour l'année du *copyright* à 2020.

En plus des paquets [KDE](https://kde.org/) [Applications 19.12.1](https://kde.org/announcements/releases/19.12.1/) qui ont commencés à arriver dans l'instantané [20200111](https://lists.opensuse.org/opensuse-factory/2020-01/msg00197.html), [Plasma 5.17.5](https://kde.org/announcements/plasma-5.17.5.php) de KDE  est également arrivé dans l'instantané. Cette mise à jour de Plasma a corrigé une régression intervenue dans la transition l'applet de pageur hors de [QtWidgets](https://doc.qt.io/qt-5/qtwidgets-index.html) et a [corrigé le glisser-déposer](https://bugs.kde.org/show_bug.cgi?id=415423) de fichiers depuis Dolphin vers un widget de bureau virtuel. Le Plasma NetworkManager avait également un [correctif pour un crash](https://bugs.kde.org/show_bug.cgi?id=415856) lors du changement de configuration [IPv4](https://en.wikipedia.org/wiki/Configurations_IPv4).

Le correctif très attendu de la vulnérabilité de sécurité dans [Firefox](https://www.mozilla.org/en-US/) a été effectué avec la mise à jour de Mozilla vers [Firefox 72.0.1](https://www.mozilla.org/en-US/firefox/72.0.1/releasenotes/); il y avait huit Common Vulnerabilities and Exposures (CVE) traitées dans la mise à jour de la version précédente [71](https://www.mozilla.org/en-US/firefox/71.0/releasenotes/) incluse dans Tumbleweed, mais la version 72.0.1 a corrigé le bogue que des pirates pouvaient utiliser pour accéder à un ordinateur de toute personne utilisant le navigateur en raison d'informations d'alias incorrectes dans le compilateur JIT [IonMonkey](https://wiki.mozilla.org/IonMonkey).

[LibreOffice](https://www.libreoffice.org/) 6.4.0.1 a ajouté un correctif pour corriger un bouton qui permettait le mauvais ordre d'une interface [Qt](https://www.qt.io/) et [curl](https://curl.haxx.se/) 7.68.0 comportait un grand nombre de correctifs et de modifications pour inclure l'ajout d'une implémentation de [BearSSL](https://bearssl.org/) vtls pour la [Transport Layer Security ](https://en.wikipedia.org/wiki/Transport_Layer_Security) (TLS).
La version 0.8.8 de snapper a bénéficié d'une réécriture d'un sous-paquet de [Python](https://www.python.org/) vers [C ++](http://www.cplusplus.com/) et plusieurs paquets [YaST](https://yast.opensuse.org/) ont été mis à jour, ce qui comprenait la correction d'une erreur lors d'une mise à niveau si `/var/lib/YaST2` manquait lors de l'utilisation de [Btrfs](https://en.wikipedia.org/wiki/Btrfs).


L'outil de dépannage [sysdig](https://github.com/draios/sysdig/releases) a été mis à jour dans l'instantané [20200110](https://lists.opensuse.org/opensuse-factory/2020-01/msg00188.html) ; il a corrigé une fuite de mémoire et mis à jour l'utilisation des [API Kubernetes](https://kubernetes.io/docs/concepts/overview/kubernetes-api/) pour prendre en charge la version 1.16.
De nombreux paquets GNOME ont été mis à jour vers la version 3.34.3 et le paquet [fwupd](https://fwupd.org/) 1.3.6, pour la mise à jour de firmware, a ajouté un nouveau plugin pour travailler avec les cartes MultiMediaCard intégrées ([eMMC](https://en.wikipedia.org/wiki/MultiMediaCard)).
Une mise à jour de rpm-build a permis l'abandon d'une dépendance à [python3-setuptools](https://pypi.org/project/setuptools/) grâce à la mise à jour de rpm en version 4.15.1 et le compilateur d'exécution optimisé pour la boucle intérieure (orc) 0.4.31 corrigé divers problèmes sur [PowerPC](https://en.wikipedia.org/wiki/PowerPC).

Les instantanés [20200109](https://lists.opensuse.org/opensuse-factory/2020-01/msg00186.html) et [20200108](https://lists.opensuse.org/opensuse-factory/2020-01/msg00177.html) contenaient une quantité minimale de mises à jour de paquets, mais le [Noyau Linux](https://www.kernel.org/) a été mis à jour vers la version 5.4.7 dans l'instantané [20200108](https://lists.opensuse.org/opensuse-factory/2020-01/msg00177.html), et fournissait une grande quantité de mises à jour par rapport au noyau 5.3.12 précédent. Les mises à jour pour Btrfs dans le noyau étaient nombreuses et il y avait une poignée de correctifs dans le noyau pour IBM [s390](https://en.wikipedia.org/wiki/IBM_System/390) et pour le système de fichiers [ext4](https://en.wikipedia.org/wiki/Ext4).
