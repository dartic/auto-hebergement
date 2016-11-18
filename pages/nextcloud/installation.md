# Installation

Pour cela, on va suivre l'install par 

<https://nextcloud.com/install/>

<https://nextcloud.com/install/#instructions-server>

## Téléchargement de nextcloud depuis la VM

    curl https://download.nextcloud.com/server/installer/setup-nextcloud.php > setup-nextcloud.php
    sudo cp setup-nextcloud.php /var/www/html
    
On utilise ici `sudo` qui nous permet de copier le fichier dans `/var/www/html`
en tant que superutilisateur.

En effet, le répertoire `/var/www/html` a été créé par l'utilisateur `root` 
et ne peut pas être écrit directement par un utilisateur 'lambda'.


## Procédure d'installation

Nous pouvons maintenant accéder à l'URL d'installation, dans mon cas ce sera :

http://192.168.1.18/setup-nextcloud.php

![Wizard 1](wizard-1.png)
![Wizard 2](wizard-2.png)

    sudo apt-get install php-xml php-curl php-zip php-mbstring php-gd

    sudo service apache2 restart
    
Nous rencontrons un problème de droit utilisateur...

![](nextcloud-dependency-fail.png)

Pour corriger ce problème, 
nous devons comprendre que le serveur HTTP Apache ne dispose pas 
de droits suffisants pour écrire dans son répertoire `/var/www/html`.

Le serveur HTTP Apache utilise l'utilisateur `www-data` 
pour écrire dans le répertoire `/var/www/html` .

Si nous regardons à qui appartient ce répertoire

    ls -l /var/www
    
![](ls-l-var-www.png)

Il appartient à `root`, le super utilisateur de la VM.

Nous allons réattribuer ce répertoire de travail à l'utilisateur `www-data` :

    sudo chown -R www-data /var/www/html
    
Puis, nous pouvons rafraîchir la page :



![Wizard 3](wizard-3.png)



Dans notre cas, on choisit de l'installer dans le répertoire courant.

Il pourrait être utile de le mettre dans un sous répertoire néanmoins.

![Wizard 4](wizard-4.png)
![Wizard 5](wizard-5.png)

![Wizard 6.1](wizard-6.1.png)
![Wizard 6.2](wizard-6.2.png)

![Wizard 5](wizard-7.png)

## La configuration avancée

via le config.php,

Par exemple, on peut changer l'application par défaut : mail

