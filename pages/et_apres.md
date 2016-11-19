# Et après ? 

L'avenir de Nextcloud est à suivre de près, mais, 
si vous avez un projet à suivre de près, je vous conseille cozy.io .

Jeune pousse, avec Tristan Nitot qui a rejoint la troupe récemment,
ce projet semble en très belle progression. 
De nombreuses apps semblent se mettre en place, 
et la qualité semble au rendez-vous.

N'hésitez pas à suivre leurs projets GitHub et y contribuer !


## Sécurisation du serveur Apache

Dans le cas où l'on met le serveur accessible sur le web, 
il sera indispensable de générer un certificat de sécurité 
certifié par une autorité de certification.
Cela permet de garantir que l'échange de données effectué
entre le navigateur web, les applications de synchronisation, 
et le serveur sont est sécurisé.

Il existe une autorité de certification automatisée,
qui a été initialement propulsé par Mozilla. 
Il s'agit de Let's Encrypt.

https://letsencrypt.org/

Un bot a été écrit, 
et est facilement installable pour chaque distribution.
Le bot se chargera de générer le certificat, 
adapter la configuration du serveur HTTP (Apache dans notre cas)
et renouveler automatiquement le certificat.

https://certbot.eff.org/

## Installation annuaire LDAP

## Installation serveur mail

Quelles sont les technos libres actuelles :
- Linagora =>
- Bluemind => solution mail / calendrier / contacts
- PostMail !... iRedMail, assemblage de divers composants

Je conseille plutôt iRedMail, paquet qui comprend beaucoup de services déjà pré installés :

http://www.iredmail.org/

Avec un petit raspberry, ça peut se faire facilement.

Il faudra alors donner une IP fixe au raspberry, 
au préalable définir la plage d'IP fixe de la box,
puis ensuite créer une redirection de port depuis la box 
pour pouvoir accéder au raspberry depuis l'extérieur.

Attention cependant, il faudra bien au préalable 
- définir un certificat de sécurité
- rediriger les flux http vers https
- définir des règles de sécurité comme un fail2ban
- monitorer les connections pour détecter toute attaque suspecte...
- définir ce que l'on considère comme une coupure acceptable (électrique, réseau,...) et le PRA / PCA dépendant

Et ça devrait marcher correctement :-)

Quelques liens :

https://yunohost.org/#/


- et pour finir...
    + le reste, le serveur de mails
    + les annuaires
    + à la maison, comment je fais ?



