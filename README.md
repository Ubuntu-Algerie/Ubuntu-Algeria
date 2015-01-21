Ubuntu-Algeria
==============

[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/Ubuntu-Algerie/Ubuntu-Algeria?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Algerian Ubuntu projects


# Installation

Cloner le projet dans votre dossier `www` en utilisant cette ligne de commande sous votre terminal (Ctrl+Alt+T):

`git clone git@github.com:Ubuntu-Algerie/Ubuntu-Algeria.git ubuntu-algerie.dev`

## Configurer le serveur web sous Ubuntu

`sudo cp /etc/apache2/sites-available/default /etc/apache2/sites-available/ubuntu-algerie.dev`

Rajoutez `ServerName  ubuntu-algerie.dev` juste apres `ServerAdmin webmaster@localhost`

Changer les lignes suivantes: 

`AllowOverride none` ==> `AllowOverride All`

`DocumentRoot /var/www` ==> `DocumentRoot /home/IDENTIFIANT/www/ubuntu-algerie.dev/app`

`<Directory /var/www/>` ==> `<Directory /home/zatamine/www/ubuntu-algerie.dev/app/>`

Ensuite activer la prise en charge du neveau host avec la commande `sudo a2ensite ubuntu-algerie.dev`

*Pour des questions de droits, backups on utilise l'espace du travail de la session en cours '/home/IDENTIFIANT'*

### Pointage du nom de domaine local

Editer ce fichier avec votre éditeur préféré.

`sudo vi /etc/hosts`

Et rajoutez cette ligne 

`127.0.0.1   ubuntu-algerie.dev`

Par convention on a choisi **ubuntu-algerie.dev**.

Maintenant lancez votre navigateur et taper le lien suivant : http://ubuntu-algerie.dev

Il ne reste plus qu'à installer Wordpresse //TODO 