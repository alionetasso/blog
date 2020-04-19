---
title: 'SUSE propose la synchronisation des flux de code, y compris les binaires SLE pour openSUSE Leap'
feed:
    limit: 10
---

SUSE a envoyé une [proposition à la communauté openSUSE](https://lists.opensuse.org/opensuse-project/2020-04/msg00002.html) pour rapprocher les flux de code de SUSE Linux Enterprise et de [openSUSE Leap]( https://en.opensuse.org/Portal:Leap). La proposition comprend des binaires SLE pour la version communautaire.

Rapprocher les flux de code pour fournir une compatibilité totale offre plusieurs avantages à la communauté pour l'avenir, tels que l'utilisation de code de meilleure qualité en raison du nettoyage des fichiers de spécifications, une relation améliorée entre les deux distributions, un rapport de bogue plus facile, moins de flux de code à maintenir, des paquets largement testés et l'inclusion d'architectures prises en charge par SLE comme s390x.

"Grâce à ce changement, nous pouvons mieux utiliser nos ressources car une seule base de code converge, donc une cible de construction de moins à considérer", a déclaré Axel Braun, membre du conseil d'administration d'OpenSUSE, dans un [e-mail envoyé à la communauté à propos de la proposition](https: //lists.opensuse.org/opensuse-project/2020-04/msg00002.html). "Tous ceux qui font des paquets pour Leap et pour Package Hub en bénéficieront immédiatement."

La proposition a fourni une approche par étapes pour la mise en œuvre de la vision. L'e-mail répertorie les options suivantes:

- Fusionner autant que possible les bases de code pour l'intersection d'OpenSUSE Leap 15.2 et de SUSE Linux Enterprise 15 SP2 sans perte de stabilité ou de fonctionnalité. (SUSE a en fait commencé à fusionner Leap avec SUSE Linux Enterprise.)
- Créer une version intermédiaire d'OpenSUSE Leap dans laquelle des binaires SLE sont utilisés à l'intérieur (période d'octobre 2020) en parallèle avec Leap 15.2 classique.
- Construire openSUSE Leap 15.3 avec les binaires SLE inclus par défaut (en supposant l'accord de la communauté).

La distribution Leap partage déjà une quantité importante de code source principal avec SLE. Leap 15.2 sera basé sur les sources de SLE 15 SP 2, mais pas sur les binaires.

La communauté discutera probablement de la proposition sur la façon d'intégrer les binaires SLE dans une nouvelle configuration de construction pour Leap et aiderait à identifier tout problème susceptible de modifier les processus ou les flux de travail. La construction du projet intermédiaire dans OBS devrait avoir lieu en mai. La construction devrait donner aux contributeurs et développeurs openSUSE l'occasion de mieux comprendre la proposition de SUSE.

"Nous avons une idée de la configuration dans build.opensuse.org", [a répondu](https://lists.opensuse.org/opensuse-project/2020-04/msg00002.html) Adrian Schröter de l'équipe OBS. "Je prévois d'avoir un premier prototype de la configuration de la construction dans les trois prochaines semaines. Nous devons garder à l'esprit que c'est vraiment une toute nouvelle façon de développer une distribution."

L'équipe de publication a évalué tous les packages et les implications techniques pour l'intégration des packages SLE supplémentaires, afin qu'ils puissent fournir une certaine clarté à la communauté sur la façon dont une implémentation technique pourrait fonctionner le mieux.

Il existe environ une douzaine de packages qui sont techniquement difficiles à implémenter pour une compatibilité totale avec les distributions d'entreprise et de communauté.

"Il a fallu un certain effort pour créer un plan acceptable par toutes les équipes impliquées", [a expliqué](https://lists.opensuse.org/opensuse-project/2020-04/msg00002.html) Lubos Kocman, responsable de la publication de Leap. "La répartition du travail entre les deux versions à venir semblait avoir été bien acceptée au moins par les parties impliquées jusqu'à présent. L'idée de la réutilisation devrait généralement réduire l'effort du côté de Leap. Cependant, cela implique le prix d'une complexité accrue à apporter toutes (les) pièces ensemble. "

Les commentaires et les discussions techniques sont une partie importante de tout projet open-source. La nouvelle version du projet intermédiaire présentera la communauté aux sources et aidera à gérer les différentes parties de code nécessaires à la mise en œuvre des planificateurs, de la publication et d'autres éléments des versions si la proposition est acceptée par la communauté.

L'équipe d'ingénierie des versions est intéressée par les commentaires des contributeurs et des utilisateurs une fois que la version intermédiaire du projet sera disponible.

La rétroaction est une partie importante de ce processus car le projet cherche à obtenir plus de code source SLE, a souligné Kocman.

Une feuille de route pour la construction du prototype d'une version proposée deviendrait disponible à [https://en.opensuse.org/openSUSE:Roadmap-2010](https://en.opensuse.org/openSUSE:Roadmap).

La foire aux questions sur ce sujet est disponible sur [https://en.opensuse.org/Portal:Leap/FAQ/ClosingTheLeapGap](https://en.opensuse.org/Portal:Leap/FAQ/ClosingTheLeapGap).

[Source](https://news.opensuse.org/2020/04/10/SUSE-proposes-synchronizing-code-streams-includes-SLE-binaries-for-openSUSE-Leap/)