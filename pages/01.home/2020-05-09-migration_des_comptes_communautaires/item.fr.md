---
title: 'Migration des comptes de la communauté'
taxonomy:
    category:
        - blog
    tag:
        - suse
        - projet
visible: false
feed:
    limit: 10
titre: 2020-05-09-migration_des_comptes_communautaires/
---

Chère communauté openSUSE,

Le système d'authentification propulsant les services suivants devrait changer ce mois-ci. Voici une liste des services susceptibles d'être affectés. Un e-mail à ce sujet a été envoyé sur la liste de diffusion du projet openSUSE. Plus d'informations sur ce sujet seront publiées sur la [Page wiki de migration de compte](https://en.opensuse.org/openSUSE:Account_Migration).

* Build Services [https://build.opensuse.org](https://build.opensuse.org)

* Bugzilla (2020-05-07 au 2020-05-10) [https://bugzilla.opensuse.org/](https://bugzilla.opensuse.org/) (qui est la même instance que bugzilla.suse.com)

Ces comptes de communauté (anciennement appelés compte Bugzilla ou compte client Novell) migrent d'un ancien système pris en charge par MicroFocus vers un nouveau système pris en charge et hébergé par SUSE.

Nous sommes en train de finaliser cette indépendance également sur le plan technique. Les comptes de la communauté (alias les comptes Bugzilla) passent maintenant d'un système fourni par MicroFocus à SUSE au centre de données de Nuremberg.

Cette action ne doit pas être confondue avec un e-mail envoyé aux utilisateurs et contributeurs avec un compte openSUSE concernant le changement de compte SUSE. L'ancienne arborescence client SUSE hébergée par MicroFocus est maintenant en transition vers le contrôle SUSE.

Il sera cependant divisé en deux parties:

1. Comptes SCC et Partner Net

Cela sera établi à partir d'une connexion hébergée par OKTA.

2. Les services openSUSE, y compris Bugzilla et OBS, mais aussi les services de développement SUSE.

Ce sera le compte qui succédera à l'ancien compte bugzilla, migré de Microfocus vers SUSE.
Il sera **nécessaire de définir un nouveau mot de passe** pour ce compte.

### Définition d'un nouveau mot de passe

Vous avez deux options pour définir un nouveau mot de passe:

#### Définissez un mot de passe via notre portail de migration

* Veuillez vous rendre sur [https://idp-migrate.opensuse.org](https://idp-migrate.opensuse.org)
* Connectez-vous avec votre ancien compte de communauté (informations d'identification Bugzilla)
* En cas de succès, vous serez redirigé vers le nouveau portail IDP et devrez définir un nouveau mot de passe

#### E-mail de réinitialisation du mot de passe (nécessite une adresse e-mail valide dans votre compte)

* Si votre compte a une adresse e-mail valide, veuillez vous rendre sur le portail IDP
* Dans le menu, sélectionnez "Mot de passe oublié" et entrez votre nom d'utilisateur pour demander un e-mail de réinitialisation de mot de passe
* Suivez les instructions dans l'e-mail pour définir un nouveau mot de passe.

Après cela, vous pouvez gérer votre compte via la migration du service IDP-Portal.

Les services utilisant les comptes de communauté migreront pas à pas. Cela signifie que pendant quelques jours, vous devez utiliser les informations d'identification anciennes et nouvelles jusqu'à la migration des services.

OBS et Bugzilla sont les premiers services à basculer le 11 mai.

En cas de problème, veuillez vérifier quel service devrait être mis à jour et migré.

