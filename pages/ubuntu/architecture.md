# Détails d'architecture

Nous avons une architecture LAMP,
ce qui signifie que nous avons :

- une machine Linux
- un serveur HTTP Apache, qui livre les pages HTML
- un interpréteur PHP, derrière le serveur HTTP, qui permet de générer des pages que le serveur HTTP va 'rendre' au navigateur
- une base de données MySQL qui va persister les données sur le disque dur de la VM

La VM dispose aussi d'un serveur SSH,
ce qui va nous permettre d'y accéder via une ligne de commande 
pour effectuer des configurations plus fines 
que ce que pourra nous permettre les outils accessibles depuis le serveur Apache.