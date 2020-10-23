# Installation custom de WordPress

## procédure d'installation : 

1. initialiser le projet composer : `composer init` => On valide avec entrée tout du long sauf pour les questions :
```
Would you like to define your dependencies (require) interactively [yes]? no
Would you like to define your dev dependencies (require-dev) interactively [yes]? no
```
ce `composer init` crée notre fichier `composer.json`.

2. 

On demande à composer d'installer le code de WordPress dans un répertoire `wp` (pas obligatoire) : 

_dans composer.json :_
```
"extra": {
        "wordpress-install-dir": "wp"
},
```
On définit une option dans le fichier composer.json pour gérer (si on veut le faire) le nom du dossier dans lequel on installera WordPress

Installer le package _johnpbloch/wordpress_ : `composer require johnpbloch/wordpress`

:warning: Il ne faut oublier d'ajouter au .gitignore (ou de le créer) :

```
/vendor
/wp
```