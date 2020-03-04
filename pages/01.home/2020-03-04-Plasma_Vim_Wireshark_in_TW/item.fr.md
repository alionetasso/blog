---
title: 'Plasma, Vim et Wireshark mis à jour dans Tumbleweed'
taxonomy:
    category:
        - blog
    tag:
        - tumbleweed
visible: false
feed:
    limit: 10
titre: 2020-03-04-Plasma_Vim_Wireshark_in_TW
---

Au total, cinq instantanés [openSUSE](https://www.opensuse.org/) [Tumbleweed](https://en.opensuse.org/Portal:Tumbleweed) ont été publiés cette semaine, ils fournissaient des mises à jour pour YaST, la version LTS de KDE Plasma et pour le système d'impression open source CUPS.

Le dernier instantané, [20200301](https://lists.opensuse.org/opensuse-factory/2020-03/msg00015.html), a mis à jour quelques bibliothèques comme *libstorage-ng*, qui a été mise à jour vers la version 4.2.65; la nouvelle version de la bibliothèque de stockage de bas niveau a ajouté la prise en charge de btrfs RAID1C, ajouté des fonctions *being* et *end* à ProbeCallbacks et mis à jour les traductions.
La mise à jour de *libyui* en 3.9.3 a supprimé les balises de groupe RPM obsolètes. Une vérification pour vous assurer que le réseau fonctionne avant de démarrer les scripts d'initialisation a été effectuée avec la mise à jour *autoyast2* 4.2.28. Un support a été ajouté pour le démarrage sécurisé d'IBM S390 avec la mise à jour du paquet *yast2-firstboot*. La mise à jour de *yast2* 4.2.67 a apporté un changement afin d'afficher les modules capables dans le centre de contrôle pour le sous-système Windows pour Linux et une mise à jour de *yast2-network* 4.2.47 à 4.2.58 a ajouté une classe pour représenter les serveurs NTP. Le cliché a actuellement une côte stable de 98, selon le [réviseur de clichés de Tumbleweed](https://review.tumbleweed.boombatower.com/).

La communauté KDE a fourni plusieurs mises à jour de paquets dans la version Plasma 5.18.2, qui est arrivée dans l'instantané [20200229](https://lists.opensuse.org/opensuse-factory/2020-03/msg00010.html).
Le paquet *libkscreen2* dans la version 5.18.2 a corrigé un bogue de kwayland de sorte qu'il attendra plus longtemps un délai de connexion et réessayera en cas d'échec. Il y avait aussi une poignée de correctifs pour Flatpak concernant la découverte d'applications et de modules complémentaires de KDE.
L'analyseur de paquets Wireshark 3.2.2 a corrigé quelques CVE pour les communications sans fil à large bande lors de plantages LTE et WiMax, ainsi qu'un correctif pour WireGuard.
Le système de fichiers XFS a reçu sa première mise à jour de version mineure dans l'instantané de *xfsprogs* 5.0.0 à 5.4.0, qui a fourni plusieurs correctifs, une refactorisation et la suppression de fonctions inutiles. Le paquet *sysconfig* 0.85.4 quant à lui a créé un lien symbolique, dans *ypbind*, qui permet aux bots de fonctionner correctement.
Cet instantané obtient une note stable de 95, selon le critique d'instantanés Tumbleweed.

Le paquet AppStream, qui est utilisé pour améliorer les métadonnées sur les composants logiciels, a été mis à jour en 0.12.10 dans l'instantané [20200228](https://lists.opensuse.org/opensuse-factory/2020-02/msg00603.html ) et il fournit quelques correctifs dont l'un restaure la compatibilité avec GLib.
L'application musicale de KDE, Amarok, a corrigé le chargement des paroles de *lyrics.wikia.com*. Le comportement d'entrée et de sortie de la recherche a été amélioré dans la mise à jour 3.34.0 de *gnome-characters* et *krb5* 1.18 a supprimé la prise en charge du chiffrement single-DES.
L'instantané a également une note stable de 98.

L'instantané [20200227](https://lists.opensuse.org/opensuse-factory/2020-02/msg00576.html) a mis à jour l'outil *dracut* et a ajouté un avertissement lors de l'inclusion de modules non pris en charge et de modules de contrôleur hôte PCI (Peripheral Component Interconnect).
Le noyau Linux a également été mis à jour vers la version 5.5.6 dans l'instantané, qui comprenait des correctifs DTS (Device Tree Source) pour l'horloge *dwmmc* dans quelques produits Rockchip.
L'instantané a un côte stable de 97.

L'instantané de [20200226](https://lists.opensuse.org/opensuse-factory/2020-02/msg00554.html) contenait quelques mises à jour de paquets importantes pour les utilisateurs comme ImageMagick 7.0.9.25 qui adaptent un changement des options en ligne de commande lors de la délégation SVG Inkscape.
Mozilla Firefox 73.0.1 a corrigé une sortie inattendue en quittant le mode « Aperçu avant impression » et résolu les problèmes de connexion au site Web de la Banque Royale du Canada (pour ceux d'entre vous qui souhaitent découvrir un jeu sympa créé sur le site Web de la Banque du Canada, cliquez sur « facturer 10$ » plusieurs fois pour voir ce qui se passe).
Le paquet *cups-filters* 1.27.1 a ajouté la prise en charge des polices chinoises/japonaises/coréennes (CJK).
*wayland* 1.18.0 a ajouté une interface de programmation d'application (API) pour marquer les objets proxy pour permettre aux applications et aux kits d'outils de partager la même connexion Wayland. D'autres mises à jour du paquet dans l'instantané ont été apportées à l'éditeur de texte *vim*, *xen*, *mariadb* 10.4.12, *gegl* 0.4.22 et *ibus* 1.5.22.
L'instantané a enregistré une note stable de 93.

GNU Compiler Collection (GCC) 10 devrait arriver dans le prochain instantané Tumbleweed et il sera utilisé comme fournisseur de bibliothèque mais pas encore comme compilateur par défaut.
