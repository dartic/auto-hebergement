# Installation d'applications

## via le bouton '+ Applications'

Accès au store d'applications 'certifiées'

- installation de calendrier
  - créer un nouvel événement pour l'utilisateur 'admin'
  - partager l'agenda à l'utilisateur 'demo' en écriture
  - mettre à jour l'événement
  - constater la mise à jour pour l'utilisateur 'admin'
- installation de contacts
  - idem que pour calendrier
- installation de stockage externe (External storage support)
  - ajouter un stockage externe depuis l'administration globale,
    et vérifier qu'il est bien accessible depuis tous les utilisateurs
  - ajouter un stockage externe depuis l'utilisateur 'demo',
    et vérifier qu'il n'est accessible que depuis l'utilisateur 'demo'
  - https://docs.nextcloud.com/server/10/admin_manual/configuration_files/external_storage_configuration_gui.html

## via les applications expérimentales 

Les applications expérimentales sont plus difficiles d'accès.

Mais ce n'est pas mission impossible !

Pour installer ces applications, 
on doit les installer manuellement dans le répertoire `apps`
de Nextcloud.

On va se placer dans ce répertoire, et on va se mettre en super utilisateur :

    cd /var/www/html/apps
    sudo su

Pour chaque application à installer, nous devons respecter cet ordre là :

  - d'abord on récupère les sources de l'application
    - `curl -L https://github.com/ORGANISATION/APP/releases/download/VERSION/APP.tar.gz > APP.tar.gz`
  - puis on dézipe
    - `gunzip APP.tar.gz`
  - on extrait l'archive
    - `tar -xf APP.tar APP`
  - on va dans le menu d'ajout d'application pour activer l'application
    - onglet `Désactivées`

Puis on va regarder ce store d'applications non certifiées :
https://apps.nextcloud.com/

### 1) installation de news, lecteur RSS

  - https://apps.nextcloud.com/apps/news
  - Fichier à récupérer : https://github.com/nextcloud/news/releases/download/9.0.4/news.tar.gz
  - ajouter deux nouveaux flux avec par exemple Gamekult et NextInpact
    - http://www.gamekult.com/cobranding/rss/news.xml
    - https://www.nextinpact.com/rss/news.xml

### 2) installation de apporder, outil pour réorganiser l'ordre des apps
  - https://apps.nextcloud.com/apps/apporder
  - Fichier à récupérer : https://github.com/juliushaertl/apporder/releases/download/0.3.3/apporder.tar.gz
  - y accéder à partir du menu

### 3) installation d'un lecteur audio
  - https://apps.nextcloud.com/apps/audioplayer
  - Fichier à récupérer : https://github.com/Rello/audioplayer/releases/download/1.3.1/audioplayer-1.3.1.tar.gz
  - ajouter des fichiers audio... échecs car limite de 2Mo...
  - => configurer PHP 
    - `sudo nano /etc/php/7.0/apache2/php.ini`
    - Rechercher avec Ctrl + W 'upload_max_filesize'
    - mettre à jour `2M` => `100M`
    - `upload_max_filesize = 100M`
    - Rechercher avec Ctrl + W 'post_max_size'
    - mettre à jour `8M` => `100M`
    - `post_max_size = 100M`
    - `sudo service apache2 restart`

### 4) installer direct menu, qui permet d'avoir une barre supérieure d'accès aux apps

  - https://apps.nextcloud.com/apps/direct_menu
  - Fichier à récupérer : https://github.com/juliushaertl/direct_menu/releases/download/v0.9.2/direct_menu.tar.gz
  - s'affiche quand largeur d'écran suffisante, sinon menu classique

### 5) installer un lecteur de mail

  - https://apps.nextcloud.com/apps/mail
  - Fichier à récupérer : https://github.com/nextcloud/mail/releases/download/v0.6.0/mail.tar.gz
  - permet de se connecter à son propre serveur mail
  - mémorise les informations de connexion
  - app pas encore assez aboutie (on ne peut pas trier ses mails, créer des dossiers)
  - mais câblée aux contacts, et assez élégante

### 6) installer un système de visio conférence

  - https://apps.nextcloud.com/apps/spreedme
  - Fichier à récupérer : https://apps.owncloud.com/CONTENT/content-files/174436-spreedme.tar.gz
  - permet de faire de la vidéo conf
  - nécessite d'avoir un serveur spreedme-server installé sur la machine
  - https://github.com/strukturag/spreed-webrtc

