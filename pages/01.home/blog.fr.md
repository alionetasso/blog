---
title: Accueil
body_classes: 'title-center title-h1h2'
dateformat: 'd-m-Y H:i'
child_type: item
visible: true
admin:
    children_display_order: collection
hero_image: alionet_blog_banner.png
content:
    items:
        - '@self.children'
    limit: 10
    order:
        by: date
        dir: desc
    pagination: true
    url_taxonomy_filters: true
feed:
    limit: 10
---

# Alionet news
Les nouvelles d'openSUSE et de sa communauté francophone
