---
title: 'Kismet et Frameworks mis à jour dans Tumbleweed'
taxonomy:
    category:
        - blog
    tag:
        - tumbleweed
visible: false
feed:
    limit: 10
titre: 2020-03-27-Kismet_Frameworks_in_TW
---

Quatre [snapshots openSUSE Tumbleweed](https://software.opensuse.org/distributions/tumbleweed) ont été publiés jusqu'à présent cette semaine.

Kismet, KDE Frameworks, sudo, LibreOffice et ImageMagick ne sont que quelques-uns des paquets qui ont reçu des mises à jour dans les instantanés.

L'instantané le plus récent, [20200322](https://lists.opensuse.org/opensuse-factory/2020-03/msg00282.html) embarquait la version 1.3.6 de l'outil de configuration Bluetooth, [blueberry](https://github.com/linuxmint/blueberry). L'outil fournissant des informations système en ligne de commande (CLI) [inxi 3.0.38](https://github.com/smxi/inxi) a corrigé un problème Perl où perl traite `000` comme une chaîne et non 0. Le VPN [WireGuard](https://www.wireguard.com/) a supprimé du [code mort](https://en.wikipedia.org/wiki/Dead_code).
L'instantané a également mis à jour plusieurs paquets [YaST](https://yast.opensuse.org/). Des corrections ont été apportées pour aider avec les icônes de texte affichées pendant les installations dans le paquet yast2 4.2.74 et certaines modifications cosmétiques ont été apportées dans le paquet yast2-ntp-client 4.2.10 pour ne pas afficher les cases à cocher pour l'enregistrement de la configuration et le démarrage du démon.
Le cliché a actuellement une côté de 84, selon le [réviseur de clichés de Tumbleweed](https://review.tumbleweed.boombatower.com/).

Seulement trois paquets ont été mis à jour dans l'instantané [20200320](https://lists.opensuse.org/opensuse-factory/2020-03/msg00274.html). La compatibilité avec Python 2 a été supprimée dans le paquet [urlscan 0.9.4](https://pypi.org/project/urlscan/).
Elementary-xfce-icon-theme et perl-Encode 3.05 ont tous deux été mis à jour dans l'instantané, qui a une côte de 99.

Les deux instantanés suivants ont également enregistré une note stable de 99.

[ImageMagick](https://imagemagick.org/index.php) 7.0.10.0 a fourni une mise à jour qui empêche [le débordement de tas](https://en.wikipedia.org/wiki/Heap_overflow) dans l'instantané [20200319](https://lists.opensuse.org/opensuse-factory/2020-03/msg00269.html).
[Frameworks 5.68.0 de KDE](https://kde.org/announcements/kde-frameworks-5.68.0.php) a corrigé une fuite de mémoire dans ConfigView et Dialog. Plusieurs ajouts et corrections ont été apportés au paquet Breeze Icons de la nouvelle version Frameworks et [Kirigami](https://kde.org/products/kirigami/) a amélioré la prise en charge Qt 5.14 sur Android.
[LibreOffice](https://www.libreoffice.org/) 6.4.2.2 a apporté quelques traductions et sudo a eu un changement mineur concernant une mise à jour qui a affecté les conteneurs Linux et ignoré un échec de restauration de la limite de ressources RLIMIT_CORE.

Les collections de compilateurs GNU (GCC) 9 et 10 ont été mises à jour dans l'instantané [20200318](https://lists.opensuse.org/opensuse-factory/2020-03/msg00262.html). Les versions mises à jour incluent des correctifs pour l'analyse des versions de binutils.
La nouvelle version majeure de [Mozilla Firefox 74.0](https://www.mozilla.org/en-US/firefox/74.0/releasenotes/) a atterri dans l'instantané et a corrigé une douzaine de vulnérabilités et d'expositions communes, qui comprenaient un correctif pour [CVE-2020-6809](https://www.mozilla.org/en-US/security/advisories/mfsa2020-08/#CVE-2020-6809) qui traitait des extensions Web qui avaient l'autorisation *all-urls* et a fait une demande de récupération avec un mode défini sur « même origine » pour que l'extension Web puisse lire les fichiers locaux.
Le paquet [Advanced Linux Sound Architecture](https://www.alsa-project.org/wiki/Main_Page) (alsa) 1.2.2 a ajouté plusieurs correctifs et la même version alsa-plugins paquet a fourni une mise à jour pour les fichiers m4 affectant la macro processeurs.
[Apparmor](https://en.wikipedia.org/wiki/AppArmor) 2.13.4 a fourni plusieurs mises à jour d'abstraction et d'analyse syntaxique des journaux pour les journaux avec une nouvelle ligne intégrée. Les développeurs seront heureux de voir un nouveau cscope 15.9 pour les recherches de code source car il ajoute les parenthèses et la barre verticale (pipe) à la liste des métacaractères utilisés dans les recherches d'expression régulière.
Les implémentations SecureTransport et WinCrypt pour sha256 ont été ajoutées dans la [curl](https://curl.haxx.se/) 7.69.1.
Une version de maintenance de [virtualbox](https://www.virtualbox.org/wiki/Downloads) 6.1.4 était dans l'instantané; la mise à jour prend en charge Linux Kernel 5.5.
Linux Kernel 5.5.9 a également été publié dans l'instantané et xfsprogs 5.5.0 a corrigé les conversions d'unités cassées dans xfs_repair.
L'outil de détection et *sniffing* de réseau et de périphérique sans fil [Kismet](https://www.kismetwireless.net/) a eu sa première version complète pour 2020, qui était principalement une version de correction de bogues; la version 2020_03_R1 avait un correctif pour les calculs de taille de tampon, ce qui pourrait avoir un impact sur la gestion du GPS, et comportait des mises à jour pour le code de capture kw41z du dispositif monopuce ultra-faible consommation et hautement intégré.