# Installation d'applications

## L'ajout d'application

### via le bouton '+ Applications', par exemple

- calendrier
- contacts

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



### via les applications expérimentales 

Store d'application :
https://apps.nextcloud.com/

Par exemple, on peut télécharger celles ci :

https://apps.nextcloud.com/apps/news

Créer un nouveau flux avec par exemple Gamekult
http://www.gamekult.com/cobranding/rss/news.xml


https://apps.nextcloud.com/apps/apporder
Permet de réordonner l'ordre des applications.

https://apps.nextcloud.com/apps/audioplayer

On ajoute des fichiers audio, limite de 2Mo

=> configuration de PHP qui limite l'upload à 2Mo,

Connexion SSH => 

    sudo vi /etc/php/7.0/apache2/php.ini
=> File upload => 100Mo
upload_max_filesize = 100M
post_max_size = 100M
    
    sudo service apache2 restart

https://apps.nextcloud.com/apps/direct_menu

Améliore l'accessibilité des apps

https://apps.nextcloud.com/apps/mail
Permet de se connecter à son propre serveur mail.
App pas encore assez aboutie (on peut pas par exemple créer des dossiers)
Mais câblé aux contacts.

https://apps.nextcloud.com/apps/ocsms

https://apps.nextcloud.com/apps/spreedme
Permet de faire de la vidéo conf, nécessite d'avoir un serveur installé sur la machine.
