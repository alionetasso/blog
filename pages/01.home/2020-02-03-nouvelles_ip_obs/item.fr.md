---
title: 'Nouvelles adresses IP pour build.opensuse.org'
date: '03-02-2020 21:00'
taxonomy:
    category:
        - blog
    tag:
        - obs
visible: false
feed:
    limit: 10
titre: 2020-02-03-nouvelles_ip_obs
---

Au cours de la [fenêtre de maintenance](https://en.opensuse.org/openSUSE:Downtime) de ce jeudi (2020-02-06), nous déplacerons les adresses IPv4 et IPv6 de [build.opensuse.org](https://build.opensuse.org). Les nouvelles adresses sont:

    195.135.221.162
    2001:67c:2178:8::162

Les personnes utilisant cette instance de l'[Open Build Service](https://build.opensuse.org/) ne devraient normalement pas le remarquer, mais si vous êtes assez fou pour avoir ajouté les anciennes adresses IP à certaines règles de pare-feu ou autres fichiers de configuration, assurez-vous de mettre à jour votre configuration en conséquence.

Veuillez noter que cela affecte également les entrées CNAME (alias) suivantes:

- [api.opensuse.org](https://api.opensuse.org)
- [obs-analyze.opensuse.org](https://obs-analyze.opensuse.org)
- [obs-grafana.opensuse.org](https://obs-grafana.opensuse.org)
- [obs-measure.opensuse.org](https://obs-measure.opensuse.org)
- [rabbit.opensuse.org](https://rabbit.opensuse.org)
- [registry.opensuse.org](https://registry.opensuse.org)
