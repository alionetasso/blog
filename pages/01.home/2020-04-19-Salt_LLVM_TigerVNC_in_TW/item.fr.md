---
title: 'Salt, LLVM et TigerVNC dans Tumbleweed'
taxonomy:
    category:
        - blog
    tag:
        - tumbleweed
visible: false
feed:
    limit: 10
titre: 2020-04-19-Salt_LLVM_TigerVNC_in_TW
---

Depuis jeudi dernier, un total de cinq instantanés [openSUSE Tumbleweed](https://software.opensuse.org/distributions/tumbleweed) ont été publiés.

Chaque instantané a mis à jour environ cinq à dix paquets.

L'instantané le plus récent, [202000414](https://lists.opensuse.org/opensuse-factory/2020-04/msg00274.html) a quelques bibliothèques mises à jour comme libgit2 0.28.5, libva 2.7.0 et libva-gl 2.7.0. Plusieurs bugs et cinq [Vulnérabilités et expositions communes](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) ont été corrigés pour le client VNC multiplateforme hautes performances [tigervnc](https://github.com/TigerVNC) 1.10.1.
Midnight Commander (mc) 4.8.24, un gestionnaire de fichiers plein écran en mode texte, a fourni de nouveaux thèmes et ajouté la coloration syntaxique pour [yabasic](https://en.wikipedia.org/wiki/Yabasic) (Yet Another BASIC). Une mise à jour mineure de la version 0.9.5 de plymouth a supprimé les en-têtes de noyau inutilisés et les dépendances de construction des modules-init-tools et les paramètres xfce4 4.14.3 ont mis à jour les traductions et modifié l'affichage pour permettre l'utilisation d'une configuration de secours. Le paquet xfwm4 4.14.1, le gestionnaire de fenêtres de l'environnement [Xfce](https://www.xfce.org/), a corrigé les noms d'hôtes qui ne s'affichaient pas initialement lors de l'exécution à distance des applications et la mise à jour a corrigé un plantage avec la bibliothèque graphique impliquant une utilisation élevée du processeur.
Le snapshot est actuellement stable, avec une note de 93, selon le [Tumbleweed snapshot reviewer](https://review.tumbleweed.boombatower.com/).

Une nouvelle version majeure du navigateur [Mozilla Firefox](https://www.mozilla.org/en-US/firefox/new/) a été publiée dans l'instantané [20200413](https://lists.opensuse.org/opensuse-factory/2020-04/msg00258.html). La [nouvelle version 75.0](https://www.mozilla.org/en-US/firefox/75.0/releasenotes/) améliore le comportement sous Linux lorsque vous cliquez sur la barre d'adresse et la barre de recherche, qui correspond désormais à d'autres bureaux: un simple clic sélectionne tout sans sélection principale; un double clic sélectionne un mot; et un triple clic sélectionne tout avec la sélection principale. De plus, Firefox est [maintenant disponible dans Flatpak](https://flathub.org/apps/details/org.mozilla.firefox) et un bug de sécurité de la mémoire pour Firefox 75 et Firefox ESR 68.7 a été corrigé.
Le paquet btrfsprogs est passé de la version 5.4.1 à la version 5.6 et prend en charge de nouveaux algorithmes de hachage dans le [noyau Linux](https://www.kernel.org/) 5.5; la nouvelle version prend également en charge les fonctionnalités LOGICAL_INO_V2 dans la résolution logique. La nouvelle option «-o» prend en charge les outils avancés de déduplication. La bibliothèque libostree 2020.3 a été mise à jour dans Tumbleweed à partir de sa précédente version 2019.6; neuf mois de mises à jour apportent plusieurs fonctionnalités et correctifs plus récents, comme la prise en charge du montage en lecture seule de `/sysroot` au démarrage, et la gestion des erreurs autour de la vérification GPG a été révisée.
L'éditeur de texte [nano](https://www.nano-editor.org/) 4.9.2 a corrigé un plantage après avoir annulé un <Enter> après un espace de début de ligne.
Le cliché a actuellement une cote modérée de 83 selon le [Tumbleweed snapshot reviewer](https://review.tumbleweed.boombatower.com/).

L'instantané [20200411](https://lists.opensuse.org/opensuse-factory/2020-04/msg00217.html) a également une tendance de 83 et a fourni moins d'une demi-douzaine de paquets mis à jour. Le paquet gnome-weather 3.34.2 de [GNOME](https://www.gnome.org/) a corrigé un bug de température et de conditions nuageuses lors de l'utilisation de l'autolocalisation.
La version yast2 4.2.81 a retraduit le bouton d'aide de l'assistant dans l'interface utilisateur [ncurses](https://en.wikipedia.org/wiki/Ncurses). Des mises à jour ont également été apportées à yast2-packager 4.2.61 et yast2-tune 4.2.3.

Le paquet [ncurses](https://en.wikipedia.org/wiki/Ncurses) a été mis à jour dans l'instantané [20200410](https://lists.opensuse.org/opensuse-factory/2020-04/msg00213.html) ; la nouvelle version a ajouté une option de configuration et une vérification de la fonctionnalité *-fvisibility=hidden* de la collection de compilateurs GNU .
L'instantané comportait également une mise à jour de gcc9 9.3.1. PCI, USB et les identifications des fournisseurs ont été mis à jour dans le paquet hwdata 0.334.
De nombreuses améliorations incrémentielles et corrections de bugs ont été apportées avec la mise à jour vers [libvirt](https://libvirt.org) 6.2.0. Le nouveau libvirt implémente une fonctionnalité QEMU 5.0 permettant la prise en charge de la mémoire [NVDIMM](https://en.wikipedia.org/wiki/NVDIMM) pour les invités pSeries, ce qui se fait en ajoutant un élément 'uuid' dans la mémoire XML qui peut soit être fourni dans le ficher XML ou, s'il est omis, généré automatiquement.
[Salt 3000](https://docs.saltstack.com/en/latest/topics/releases/3000.html) est arrivé dans Tumbleweed; la nouvelle version Salt supprime le versionnage de la date, fournit de nouvelles fonctions à chroot: apply, sls et highstate. Il met également à jour la syntaxe des emplacements pour prendre en charge l'analyse des réponses du dictionnaire et pour ajouter du texte.
L'instantané enregistrera probablement une note modérée de 82 selon le [réviseur d'instantanés Tumbleweed](https://review.tumbleweed.boombatower.com/).

L'instantané [20200409](https://lists.opensuse.org/opensuse-factory/2020-04/msg00211.html) a enregistré une note de 82 et fourni une mise à jour de [flatpak](https://flatpak.org/) 1.6 .3, qui a corrigé une régression dans le calcul de la progression pour les applications utilisant des données supplémentaires. L'utilitaire [strace 5.6](https://github.com/strace/strace/releases) a apporté plusieurs améliorations, comme la possibilité de désactiver des messages spécifiques à l'aide de *-e quiet / -quiet* (un alias pour l'option -q) , y compris ceux qui ne pouvaient pas être réduits au silence auparavant (messages de résolution de chemin d'accès et "remplacés par execve"). Un autre paquet remarquable mis à jour dans l'instantané était la mise à jour du compilateur LLVM; [llvm10 10.0.0](https://releases.llvm.org/10.0.0/docs/ReleaseNotes.html) apporte de nouveaux outils comme llvm-ifs, llvm-install-name-tool et llvm-Reduce.
