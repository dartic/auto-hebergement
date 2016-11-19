# Et après ?

Après, on lézarde... avec ce temps, dur !

Après, j'aurais pas mal de choses à vous raconter, c'est sûr...

Notamment que si cela vous intéresse, 
un peu de veille ne fait pas de mal pour savoir 
quelles sont les solutions d'hébergement à suivre de près...

Bien sûr, Nextcloud est à suivre, mais, 
je vous conseille de regarder aussi cozy.io .

Né fin 2012, cozy.io est un développement français,
qui propose un système d'hébergement privé similaire à Nextcloud.
Ce projet semble bien progresser en ce moment, et, fait marquant, 
Tristan Nitot a rejoint la troupe récemment en tant que CPO.

N'hésitez pas à suivre leurs projets GitHub et y contribuer !


## Sécurisation du serveur Apache

J'oubliais... 
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

## Installation serveur mail

Les fichiers, c'est bien.

Mais, le nerf de la guerre à mon sens, c'est plutôt les mails...

De nombreuses solutions sont le marché, mais, 
sur ce besoin, j'avertis à nouveau : **attention, fonctionnalité critique !!!!**

Un cloud qui tombe en panne pénalise les utilisateurs, 
mais il n'y a probablement pas ou peu de perte d'information.

Quand un serveur mail tombe, s'il n'a pas de serveur de secours, 
ou de rétention, les mails qui lui sont adressés peuvent se perdre 
rapidement dans la nature.

Là, à mon sens, clairement, on ne joue plus dans la même cour.

Néanmoins, je peux conseiller l'utilisation d'iRedMail, 
paquet qui comprend beaucoup de services déjà pré installés 
comme Spam Assassin, fail2ban, ...

Des éditeurs français comme Bluemind et Linagora proposent aussi
des solutions intéressantes.

## J'ai un raspberry, ça se tente ?

Bien sûr !

Tant qu'il n'y a pas de fonctionnalité critique !

Ou alors, il faut assumer les risques.

Il faudra alors donner une IP fixe au raspberry, 
au préalable définir la plage d'IP fixe de la box,
puis ensuite créer une redirection de port depuis la box 
pour pouvoir accéder au raspberry depuis l'extérieur.

## Installation annuaire LDAP

Dans la suite de l'auto-hébergement,
plus on va aller loin dans la pieuvre de services qu'on souhaite héberger,
plus vite il faudra intégrer un système d'authentification partagé.

Ce sera le moment alors de regarder du côté de LDAP, 
qui est un annuaire d'utiliateurs.

Les solutions comme Nextcloud ou iRedMail savent communiquer facilement
avec un annuaire LDAP.

Mais son installation méritera quelques petites pages de ce guide...
S'il y a des amateurs... qu'ils se manifestent !


Attention cependant, il faudra bien au préalable 
- définir un certificat de sécurité
- rediriger les flux http vers https
- définir des règles de sécurité comme un fail2ban
- monitorer les connections pour détecter toute attaque suspecte...
- définir ce que l'on considère comme une coupure acceptable (électrique, réseau,...) et le PRA / PCA dépendant

Et ça devrait marcher correctement :-)

Quelques liens :

https://yunohost.org/#/