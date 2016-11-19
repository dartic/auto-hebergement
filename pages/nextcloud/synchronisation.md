# La synchronisation

La solution d'hébergement privé Nextcloud est 'batteries included'.

On a ainsi accès à des outils de synchronisation au niveau :

- desktop
  - pour les fichiers, avec le protocole WebDAV
  - il s'agit du client de synchronisation d'ownCloud
  - https://owncloud.com/download#desktop-clients
  - ajout d'un fichier, et vérification qu'il est bien modifié des deux côtés
- smartphone / tablettes
  - pour les fichiers, avec le protocole WebDAV
    - c'est l'application Nextcloud
    - à télécharger 
      - par ici https://play.google.com/store/apps/details?id=com.nextcloud.client
      - ou par là https://apkpure.com/nextcloud/com.nextcloud.client
    - facile d'utilisation, permet de se synchroniser avec plusieurs nextcloud
    - et permet l'ajout automatique des photos par exemple
  - pour les calendriers et contacts, avec le protocole CardDAV et CalDAV
    - c'est l'application EasyDAV
    - à télécharger
      - par ici https://play.google.com/store/apps/details?id=com.bodeme.easycloud
      - ou par là https://apkpure.com/easy-dav-for-owncloud/com.bodeme.easycloud


https://software.opensuse.org/download/package?project=isv:ownCloud:desktop&package=owncloud-client




https://docs.nextcloud.com/server/10/user_manual/files/access_webdav.html#nextcloud-desktop-and-mobile-clients 

https://docs.nextcloud.com/server/10/user_manual/files/access_webdav.html#accessing-files-using-microsoft-windows


Et la découverte de leur fonctionnement, via le web,
ou via une app Android qui permet de câbler son calendrier,
Grâce à Easy DAV for ownCloud (à télécharger).

> Démo de synchronisation d'événement du calendrier, 
> Peut être à voir aussi avec un agenda 'public' où les gens pourraient en direct mettre des events.

## stockage externe


Attention, si synchronisation avec des applications desktop / mobile,
penser à ne pa synchroniser ces dossiers là.

