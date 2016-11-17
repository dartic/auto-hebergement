# Installation de Ubuntu Server

## Téléchargement
On va télécharger la version serveur, accessible ici :

<https://www.ubuntu.com/server>

L'idée de partir sur une version serveur est d'avoir une machine plus légère
qu'une machine intégrant les processus d'affichage graphique.

Les pages suivantes détaillent les différentes étapes 
pour aboutir à l'installation d'un serveur ubuntu,
préconfiguré pour accueillir une installation de la solution Nextcloud.

## Langage / Composants / Réseau

![Choix du langage](./1.png)
![Chargement des composants supplémentaires](./2.png)
![Configurer le réseau](./3.png)

-----------

## Utilisateurs / Horloge

![Création](./4.png)
![Mot de passe](./5.png)
![Chiffrage](./6.png)
![Configurer l'horloge](./7.png)

-----------

## Partitionnement des disques

![Partitionner les disques](./8.png)
![Phrase secrète](./9.png)
![Quantité d'espace](./10.png)
![Quantité d'espace](./11.png)
![Quantité d'espace](./12.png)
![Quantité d'espace](./13.png)
![Quantité d'espace](./14.png)
![Quantité d'espace](./15.png)
![Quantité d'espace](./16.png)
![Quantité d'espace](./10.png)
![Quantité d'espace](./10.png)
![Quantité d'espace](./10.png)
## Pour terminer l'installation

Installation de openssh-server

    sudo apt-get install openssh-server
    sudo service ssh start

