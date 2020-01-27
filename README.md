# Manuel du rédacteur Alionet

## Généralités

Depuis la refonte de novembre 2019, Alionet dispose d'un [forum](https://www.alionet.org) et d'un [blog](https://blog.alionet.org) séparés.
Le moteur du blog est [Grav](https://getgrav.org), un CMS simple, utilisant PHP mais dont la configuration se fait en fichier *Yaml* et dont les articles sont écrits en *Markdown*, un langage à balise très simple à utiliser.

La rédaction des articles peut se faire de 2 façons différentes:

* directement depuis [l'interface de rédaction](https://blog.alionet.org/admin)
* depuis votre poste puis en *poussant* votre article sur le [dépôt Git](https://github.com/alionetasso/blog) de l'association Alionet

## Écrire un article depuis l'interface Web

Pour pouvoir se connecter, il faut disposer d'un compte rédacteur (en faire la demande à un administrateur) et se rendre à l'adresse [https://blog.alionet.org/admin](https://blog.alionet.org/admin).

* Cliquer ensuite sur le lien **Pages** dans la barre latérale à gauche

* Cliquer sur **Ajouter** dans la barre supérieure, à droite

![](./01.png)

* Dans le menu de création qui s'affiche, il convient de renseigner les éléments et options suivants:

    * Le titre de la page: c'est le nom de votre article
    * Le nom du dossier: il a été déduit automatiquement du nom de l'article, c'est dans ce dossier que Grav va ranger l'article sur le serveur, vous n'avez pas à vous en soucier
    * Page parente: il faut sélectionner **(home) Accueil**
    * Template de page: il faut choisir **Item**
    * Visible: Cliquer sur **Non**, sans cela l'article sera visible dans le menu du blog alors que nous voulons qu'il soit créé comme *enfant* de la page principale

![](./02.png)

* Une fois les paramètres ci-dessus validés, nous allons pouvoir commencer la rédaction de l'article:

![](./03.png)

Le format employé est le [Markdown](https://commonmark.org/help/), se référer à ce lien pour voir les balises à utiliser.
Pour ajouter une image d'en-tête de l'article, pas besoin de l'ajouter via un lien, il suffit d'enregister une première fois votre article pour que Grav vous permette de l'ajouter.

La première image trouvée sera automatiquement utilisée en tant qu'illustration de l'article. Il n'est pas non plus nécessaire de mettre un titre à l'article, Grav s'en charge.
Une fois l'article rédigé, il suffit de l'enregistrer pour qu'il soit visible en ligne sur la page d'accueil du blog. Vous pouvez contrôler le rendu final en cliquant sur l'icône **Œil** dans la barre de mise en forme.

Il faut savoir que lorsque vous enregistrer votre travail, Grav va automatiquement le pousser dans le dépôt Git.

L'article est ensuite disponible:

![](./04.png)

## Utiliser Git

Cette page décrit le flux de travail à suivre pour l'utilisation de Git en vue d'éditer le contenu de ce dépôt.

### Configuration de Git

Il est important que Git soit bien configuré afin que les commits soient identifiés clairement et proprement.
En voici un exemple, contenant entre autres choses des *alias*.

```
[user]
	name        = Sogal
	signingkey  = sogal@volted.net
	email       = sogal@volted.net
[commit]
    gpgSign     = True
[push]
	default     = simple
[alias]
	co          = checkout
	ci          = "commit -a -m"
	st          = status
	br          = "!git --no-pager branch"
	df          = diff
	pl          = pull
    pu          = push
[core]
[core "pager"]
	log         = less
	blame       = less
	branch      = cat
```

### Clé SSH

Une fois que l'admin a créé le compte sur le dépôt Git, il faut s'y connecter et ajouter sa clé SSH dans les paramètres du compte.
Si vous n'avez pas de clés SSH, il faut en créer une comme suit:

```
[ ! -d $HOME/.ssh ] && mkdir $HOME/.ssh
cd $HOME/.ssh
ssh-keygen -t rsa -b 4096 -f my_ssh_key.rsa
```

On vous demande une phrase de passe qui chiffre la clé qui va être créée et évite son utilisation fraduleuse en cas de compromission de la machine.

### Récupération des sources

#### Pour la 1ère fois

```
git clone git@git@github.com:alionetasso/blog.git
```
#### Pour mise à jour

```
git pull
```

#### Ajouter un fichier

Pour faire en sorte que Git puisse suivre les modifications d'un nouveau fichier, il faut:

```
git add chemin/vers/nouveau_fichier
```

#### Enregistrer les modifications

Maintenant que vous avez modifier/ajouter, il faut valider tout ça (`commit` en anglais) et ajouter un message expliquant brièvement la modification:

```
git commit -am "mise à jour des liens dans la page xxx"
```

### Pousser les modifications

Vous pouvez ensuite rendre publique votre contribution via :

```
git push
```

## Markdown

À toute fin utile, voici un rappel de la syntaxe Markdown utilisée pour l'édition de l'ensemble des pages de ce wiki :

### Titre de page

```
Titre de ma page
================
```

### Niveau de titres

```
# Grand titre
## Titre secondaire
### Petit titre
```

### URL

```
[Texte de l'adresse](http://mon.url.tld)
ou en interne
[Texte de l'adresse interne](docs/page.md)
```

### Mise en forme du texte

```
*italique*
**gras**
```

### Code

    ```
    code
    ```
ou

`code en ligne`

### Image

```
![Texte de l'image aka. alt](chemin/vers/image)
```

Plus d'exemple sur la [page de syntaxe Markdown](https://daringfireball.net/projects/markdown/syntax).

### Table

```
Colonne 0 | Titre col.1 | Autre col.3
----------|-------------|-------------
Contenu   | Très long contenu dans cette colonne | Dernière colonne
Encore | une | ligne
Et puis | | la dernière ligne
```

Colonne 0 | Titre col.1 | Autre col.3
----------|-------------|-------------
Contenu   | Très long contenu dans cette colonne | Dernière colonne
Encore | une | ligne
Et puis | | la dernière ligne

### Convertir le Markdown

Installer le paquet `pandoc`:

```
zypper in pandoc
```

Lancer la conversion vers du *html* :

```
pandoc -f markdown+hard_line_breaks -t html -s -o md-preview.html fichier.md
```

### Astuces Markdown pour Vim

Parce qu'éditer du Markdown avec Vim, c'est l'assurance d'une place au paradis du grand [Monstre en spaghetti volant](https://fr.wikipedia.org/wiki/Pastafarisme), voici quelques astuces pour faciliter la vie :

#### Raccourcis pour le gras et l'italique

```
" format markdown files
" F2 pour mettre la ligne en gras
autocmd FileType markdown nnoremap <F2> <Esc> I**<Esc>A**<Esc>
" F3 pour mettre la ligne en italique
autocmd FileType markdown nnoremap <F3> <Esc> I*<Esc>A*<Esc>
```

#### Gérer le *filetype*, générer un aperçu dans Firefox (via conversion avec Pandoc)

```
" markdown options
" Définir le type de fichier en fonction de l'extension
autocmd BufNewFile,BufReadPost *.md set filetype=markdown
let g:markdown_fenced_languages = ['html', 'python', 'bash=sh']
" Appuyer sur 2 puis sur m immédiatement créer la conversion en html et affiche le rendu
au BufNewFile,BufRead *.md map 2m :w<CR>:!pandoc -f markdown+hard_line_breaks -t html -s -o /tmp/vim-md-preview.html "%" ; firefox "file:///tmp/vim-md-preview.html" & <CR><CR>
```
