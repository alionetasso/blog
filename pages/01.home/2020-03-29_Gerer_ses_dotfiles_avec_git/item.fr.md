---
title: 'Gérer ses dotfiles avec Git'
taxonomy:
    category:
        - blog
    tag:
        - git
        - shell
visible: false
feed:
    limit: 10
titre: 2020-03-29_Gerer_ses_dotfiles_avec_git
---

## Dot quoi ???

Ce que l'on appelle communément *dotfiles* sont tous ces petits fichiers texte qui contiennent la configuration de certains de vos logiciels. La plupart d'entre eux se touvent dans votre `$HOME` mais sont masqués car préfixés par un point (*dot* en anglais, d'où leur nom). Pour d'autres applications vous les trouverez dans `$HOME/.config`.

En ce qui concerne leur gestion, c'est-à-dire le suivi des changements, leur sauvegarde, leur déplacement et copie entre ordinateurs...), il existe plusieurs solutions:

* la bonne vieille clé USB
* rsync
* les copier dans le "cloud"
* les copier dans un dossier central et créer des liens symboliques vers leur emplacement d'origine

Dans cet article, nous nous concentrerons sur une façon simple et efficace de faire ça grâce à [Git](https://git-scm.com/).

## Git à la rescousse

Dans cet exemple, nous utiliserons `$HOME/Dotfiles` en tant que dossier du dépôt Git mais vous êtes libres d'utiliser ce que vous voulez.

Tout d'abord, initialisons le dépôt:

    git init --bare $HOME/Dotfiles

Ensuite, dans la mesure où toutes les commandes `git` que nous allons utiliser se réfèrent à ce dépôt, il est conseillé de créer un alias tel que:

    alias dotfiles='/usr/bin/git --git-dir=$HOME/Dotfiles --work-tree=$HOME'

Vous pouvez ajouter cette ligne dans le fichier de configuration de votre $SHELL (`$HOME/.bashrc` si vous utilisez [Bash](https://www.gnu.org/software/bash/) ou `$HOME/.zshrc` si vous utilisez [zsh](https://www.zsh.org/)).

Nous allons maintenant configurer Git pour qu'il ne montre pas toute la liste des fichiers non suivis. C'est nécessaire car nous utilisons ici tout le `$HOME` en tant qu'arborescence de travail.

    dotfiles config --local status.showUntrackedFiles no

À ce stade, vous devriez être en mesure de vérifier l'état du dépôt:

    dotfiles status

Il est temps d'ajouter vos fichiers de configuration et de valider (*commit*) vos ajouts. Ajoutons par exemple notre `.bashrc` :

    dotfiles add .bashrc
    dotfiles commit -m "Added .bashrc"

Enfin, il faut ajouter un dépôt distant (votre instance auto-hébergée ou un service public tel que GitLab ou Github) puis y pousser vos changements:

    dotfiles remote add origin git@yourgit.example.com/dotfiles.git
    dotfiles push

## Configurer une nouvelle machine

Maintenant que tout est correctement configuré, voyons comment déployer ces fichiers sur une nouvelle machine:

Tout d'abord, il faut clôner le dépôt distant sur la machine en question:

    git clone --bare git@yourgit.example.com/dotfiles.git $HOME/Dotfiles

Là aussi, il est utile et recommandé de définir le même alias que précédemment:

    alias dotfiles='/usr/bin/git --git-dir=$HOME/Dotfiles --work-tree=$HOME'

Rappelez-vous d'ajouter cette ligne d'alias au fichier de configuration de votre `$SHELL`.
Ceci fait, il suffit d'appliquer les changements via une simple command:

    dotfiles checkout

Notez que si certains des fichiers devant être déployés existant déjà, vous obtiendrez un message d'erreur. Cela arrivera probablement avec des fichiers créés par défaut dans le cadre d'une installation openSUSE classique, tel que le fichier `$HOME/.bashrc`. Pas d'inquiétudes, il suffit de les renommer ou de les supprimer.

À partir de maintenant, à chaque changement dans un des fichiers suivis par Git, rappelez-vous de valider et pousser vos changements.

## Sources

Les articles suivants ont servis de sources à celui-ci. Merci à leurs auteurs:
* [Easily manage your dotfiles with git](https://lord.re/en/posts/62-dotfiles-home-git/)
* [How to make your Dotfile management a painless affair](https://www.freecodecamp.org/news/dive-into-dotfiles-part-2-6321b4a73608/)
* [How to manage your dotfiles with git](https://medium.com/toutsbrasil/how-to-manage-your-dotfiles-with-git-f7aeed8adf8b)

