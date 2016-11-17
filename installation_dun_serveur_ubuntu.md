# Installation d'un serveur Ubuntu

On va télécharger la version serveur, accessible ici :

https://www.ubuntu.com/server

L'idée de partir sur une version serveur est d'avoir une machine sans IHM pour ne pas surcharger la machine de la gestion graphique.

On pourra monitorer la machine avec d'autres services si besoin.

-----------

## Langage / Composants / Réseau

![Choix du langage](./1-install-ubuntu-server/1.png)
![Chargement des composants supplémentaires](./1-install-ubuntu-server/2.png)
![Configurer le réseau](./1-install-ubuntu-server/3.png)

-----------

## Utilisateurs / Horloge

![Création](./1-install-ubuntu-server/4.png)
![Mot de passe](./1-install-ubuntu-server/5.png)
![Chiffrage](./1-install-ubuntu-server/6.png)
![Configurer l'horloge](./1-install-ubuntu-server/7.png)

-----------

## Partitionnement des disques

![Partitionner les disques](./1-install-ubuntu-server/8.png)
![Phrase secrète](./1-install-ubuntu-server/9.png)
![Quantité d'espace](./1-install-ubuntu-server/10.png)

-----------

## Pour terminer l'installation

Installation de openssh-server

    sudo apt-get install openssh-server
    sudo service ssh start