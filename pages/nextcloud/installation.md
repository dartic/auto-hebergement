# Installation

## Téléchargement de nextcloud depuis la VM

    curl https://download.nextcloud.com/server/installer/setup-nextcloud.php > setup-nextcloud.php
    cp setup-nextcloud.php /var/www/html

On va le copier dans le répertoire /var/www, mais erreur de droits...

On va changer les droits du répertoire (propriétaire et groupe).

    sudo chown -R www-data /var/www
    sudo chgrp -R www-data /var/www

On va se rajouter aux utilisateurs du groupe www-data

    cp setup-nextcloud.php /var/www/html


## Procédure d'installation

http://192.168.1.17/setup-nextcloud.php

![Wizard 1](wizard-1.png)
![Wizard 2](wizard-2.png)

    sudo apt-get install php-xml php-curl php-zip php-mbstring php-gd

    sudo service apache2 restart

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

