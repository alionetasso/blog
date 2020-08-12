---
title: 'Gérer son onduleur APC sous openSUSE'
taxonomy:
    category:
        - blog
    tag:
        - matos
visible: false
feed:
    limit: 10
titre: 2020-08-11-gestion_apcbackup
---

Afin de protéger votre installation informatique des surtensions et pannes électriques, il peut être utile de la raccorder à un onduleur. Il est même possible de relier cet onduleur à votre installation openSUSE afin de le gérer au mieux.

Cet article fait suite à [un fil sur le forum](https://www.alionet.org/index.php?topic=311) où il est question d'un APC Back-UPS ES 550. Cela doit toutefois être facilement transposable pour tout onduleur APC connecté avec un port USB pour la communication avec le PC.

## Mise en place

Tout d'abord, on installe APCUPSD :

    sudo zypper in apcupsd

Puis on crée un fichier de configuration dans `/etc/default/apcupsd` par la commande :

    sudo $EDITOR /etc/default/apcupsd

dans lequel on ajoute la ligne suivant dans ce fichier :

    ISCONFIGURED=yes

## Configuration du service

On configure maintenant le démon *apcupsd* en éditant le fichier `/etc/apcupsd/apcupsd.conf`:

    sudo $EDITOR /etc/apcupsd/apcupsd.conf

Chercher et modifier les variables suivantes comme indiqué ci-dessous (noter DEVICE reste vide pour ES550G en usb) :

    UPSNAME ES550G
    UPSCABLE usb
    UPSTYPE usb
    DEVICE
    NISIP 127.0.0.1


On peut maintenant démarrer et activer le service avec la commande:

    sudo systemctl enable --now apcupsd

## Test

Il est enfin possible de tester que tout fonctionne correctement:

    sudo apcaccess status

ce qui devrait retourner quelque chose comme:

    APC      : 001,034,0836
    DATE     : 2020-08-10 21:06:43 +0200 
    HOSTNAME : hostname.dom.tld
    VERSION  : 3.14.14 (31 May 2016) suse
    UPSNAME  : ES550G
    CABLE    : USB Cable
    DRIVER   : USB UPS Driver
    UPSMODE  : Stand Alone
    STARTTIME: 2020-08-10 19:10:20 +0200 
    MODEL    : Back-UPS ES 550G
    STATUS   : ONLINE
    LINEV    : 240.0 Volts
