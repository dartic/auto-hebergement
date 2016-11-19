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

## via les applications expérimentales 

Les applications expérimentales sont plus difficiles d'accès.

Mais ce n'est pas mission impossible !

Accès au store d'application non certifiées :
https://apps.nextcloud.com/

- installation de news, lecteur RSS
  - https://apps.nextcloud.com/apps/news
  - ajouter un nouveau flux avec par exemple Gamekult
  - http://www.gamekult.com/cobranding/rss/news.xml
- installation de apporder, outil pour réorganiser l'ordre des apps
  - https://apps.nextcloud.com/apps/apporder
  - y accéder à partir du menu
- installation d'un lecteur audio
  - https://apps.nextcloud.com/apps/audioplayer
  - ajouter des fichiers audio
  - limite de 2Mo...
  - => configurer PHP
  - `ssh user@192.168.1.18` + mdp `capitoledulibre`
  - `sudo nano /etc/php/7.0/apache2/php.ini`
  - Rechercher avec Ctrl + W 'upload_max_filesize'
  - mettre à jour `2M` => `100M`
  - `upload_max_filesize = 100M`
  - Rechercher avec Ctrl + W 'post_max_size'
  - mettre à jour `8M` => `100M`
  - `post_max_size = 100M`
  - `sudo service apache2 restart`

https://apps.nextcloud.com/apps/direct_menu

Améliore l'accessibilité des apps

https://apps.nextcloud.com/apps/mail
Permet de se connecter à son propre serveur mail.
App pas encore assez aboutie (on peut pas par exemple créer des dossiers)
Mais câblé aux contacts.

https://apps.nextcloud.com/apps/ocsms

https://apps.nextcloud.com/apps/spreedme
Permet de faire de la vidéo conf, nécessite d'avoir un serveur installé sur la machine.

Et la découverte de leur fonctionnement, via le web,
ou via une app Android qui permet de câbler son calendrier,
Grâce à Easy DAV for ownCloud (à télécharger).

> Démo de synchronisation d'événement du calendrier, 
> Peut être à voir aussi avec un agenda 'public' où les gens pourraient en direct mettre des events.
## L'ajout de stockage externe

Via l'application 

https://docs.nextcloud.com/server/10/admin_manual/configuration_files/external_storage_configuration_gui.html

Attention, si synchronisation avec des applications desktop / mobile,
penser à ne pa synchroniser ces dossiers là.

## fonctionnement des applications



