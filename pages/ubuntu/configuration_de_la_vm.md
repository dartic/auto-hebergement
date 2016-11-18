# Configuration de la VM

## Mise en état de marche de la VM

On ne peut pas encore accéder à la VM depuis notre navigateur.

Si on fait un `ifconfig` en ligne de commande sur la VM, 


que l'on prend l'IP en 10.x.x.x, 
et qu'on la rentre sur un navigateur en http://10.x.x.x, aucune réponse.

Idem pour le ping.

Nous devons configurer l'accès réseau de la VM.

- configuration de la carte réseau en bridge / pont

<http://askubuntu.com/questions/237461/how-do-i-access-ubuntu-server-running-in-virtualbox-from-outside#237467>

![Network as a bridge](virtual-box-reseau-bridge.png)

## Sécurisation du serveur Apache

https://certbot.eff.org/

## Augmentation de la taille d'upload

