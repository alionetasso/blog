---
title: 'KDE et openSUSE: Plasma 5.17, Qt 5.14 plus encore'
date: '13-10-2019 11:38'
taxonomy:
    category:
        - blog
    tag:
        - tumbleweed
        - kde
feed:
    limit: 10
---

### Plasma 5.17 Beta

La version bêta de [Plasma 5.17](https://kde.org/announcements/plasma-5.16.90.php) a été publiée avec de nombreuses nouvelles fonctionnalités et améliorations telles que la mise à l'échelle fractionnelle par écran sur [Wayland](https://wayland.freedesktop.org/), une nouvelle interface utilisateur pour la configuration des autorisations des périphériques Thunderbolt et des statistiques réseau dans [KSysGuard](https://userbase.kde.org/KSysGuard). Ce dernier nécessite plus de privilèges que d'habitude pour une application utilisateur. C'est pourquoi l'équipe de sécurité [SUSE](https://www.suse.com/) est en train de vérifier ces autorisations.

[openQA](http://open.qa/) a déjà trouvé quelques bogues, comme [GIMP](https://www.gimp.org/) plus "[en couleurs](https://bugs.kde.org/show_bug.cgi?id=412331)" que d'habitude et certaines applications telles que [Kirigami](https://en.wikipedia.org/wiki/Kirigami) et Qt Widgets qui casse certains [raccourcis clavier](https://bugs.kde.org/show_bug.cgi?id=411758). Les deux ont été corrigés dans l’intervalle et seront corrigés dans la version finale de 5.17.

Si vous n'avez pas encore testé Plasma 5.17 Beta, il reste encore un peu de temps! Si vous rencontrez un problème dans le logiciel, veuillez vous rendre sur [KDE bug tracker](https://bugs.kde.org/). Si au lieu de cela vous trouvez un problème spécifique à [openSUSE](https://www.opensuse.org/), rendez vous sur l'[openSUSE bugzilla](https://bugzilla.opensuse.org).

Pour obtenir Plasma 5.17 sur votre installation [Leap](https://software.opensuse.org/distributions/leap) ou [Tumbleweed](https://software.opensuse.org/distributions/tumbleweed), vous pouvez lire <https://fr.opensuse.org/SDB:KDE_repositories>.

Si vous rencontrez des problèmes graves, l’instantané automatique du système de fichiers racine pris à l’aide de [btrfs](https://en.wikipedia.org/wiki/Btrfs) vous aide à revenir à l’état de fonctionnement en démarrant dans un instantané plus ancien et en faisant une restauration.

[Argon](https://en.opensuse.org/SDB:Argon_and_Krypton), un support live installable comprenant Leap 15.1 avec la version bêta et ne nécessitant aucun ajout de dépôt manuel, est également disponible.

### openSUSE Leap 15.2

Comme ce fut le cas pour Leap 42.2, 15.2 inclura également des mises à jour majeures de nombreux composants.

A côté d'une nouvelle version du [noyau Linux](https://www.kernel.org/), il est prévu de la livrer avec [Qt 5.12](https://www.qt.io/qt-5-12) LTS, Plasma 5.18 (bien sûr également LTS) et les dernières versions de [KDE Frameworks](https://kde.org/products/frameworks/) et [Applications](https://kde.org/applications/), que nous pourrons faire entrer suffisamment tôt pour que les tests appropriés garantissent la meilleure expérience utilisateur possible!

Cela signifie que la session "Full Wayland" qui a atterri dans Tumbleweed il y a quelques semaines sera également disponible dans Leap 15.2 de même que la [prise en charge de la mise à l'échelle fractionnelle par écran](https://lists.opensuse.org/opensuse-factory/2019-09/msg00177.html).

Comme les versions cibles d'Applications, Frameworks et Plasma ne sont pas encore connues, nous intégrons actuellement Qt 5.12 LTS aux derniers packages de Factory.

### Qt 5.14

Les utilisateurs de Tumbleweed et de Leap sont habitués à bénéficier des versions les plus récentes des logiciels KDE incluant les fonctionnalités et corrections de bogues disponibles, ce qui n'est possible qu'en suivant le développement de Qt et en agissant de manière proactive.

Ainsi, bien que la branche 5.1 de Qt soit encore jeune, nous sommes déjà en train de l'intégrer dans nos versions. Lors de la construction initiale de la version 5.14 Alpha, certains bogues (QTBUG-78867, QTBUG-78881, QTBUG-78911, QTBUG-78948) avaient déjà été identifiés et corrigés pour la plupart, de sorte que le projet [KDE:Qt:5.14](https://build.opensuse.org/project/show/KDE:Qt:5.14) est construit et utilisable dès maintenant. Pour développer avec Qt 5.14 et tester vos applications, vous n'avez plus qu'à ajouter le dépôt.

Jusqu'ici, nous en sommes toujours à la phase d'intégration et nous préparons tout ce qui doit l'être, mais nous soumettrons bientôt Qt 5.14 en zone de transit de [Factory](https://fr.opensuse.org/Portal:Factory) afin de voir comment il s'y intègre.

L'une des caractéristiques les plus visibles pour l'utilisateur est que la [mise en œuvre de la mise à l'échelle](https://lists.qt-project.org/pipermail/development/2019-September/037434.html) (pour les écrans HiDPI) a été principalement réécrite. Parmi les autres changements notables, citons l'ajout de divers systèmes d’accélération de Qt Quick utilisant une nouvelle [couche d’abstraction](https://en.wikipedia.org/wiki/Abstraction_layer) (opt-in), qui peut désormais tirer parti de [Vulkan](https://en.wikipedia.org/wiki/Vulkan_(API)) ainsi que l'introduction d'un nouveau module "[qtquicktimeline](https://github.com/qt/qtquicktimeline)", qui permet de faciliter intégration d'animations basées sur la chronologie dans Qt Quick.