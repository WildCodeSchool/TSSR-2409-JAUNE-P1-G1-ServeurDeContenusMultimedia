# TSSR-2409-JAUNE-P1-G1-ServeurDeContenusMultimedia

# Présentation du projet
Notre projet vise à mettre en place un serveur de gestion de contenus multimédia robuste et efficace. L'objectif principal est de créer une plateforme centralisée pour stocker, organiser et diffuser divers types de médias numériques.

## Introduction : 
Dans un monde où la consommation de contenus multimédias ne cesse d’augmenter, il devient essentiel pour les entreprises et les particuliers de disposer d'une solution centralisée pour gérer leurs médias numériques. Ce projet répond à ce besoin en proposant une plateforme flexible et performante, capable de s'adapter à différents environnements et besoins.

## Membres du groupe :
Baudouin Soubrier De Gaudemar (Product Master durant le 1er sprint)
Erwan Salomon (Scrum Master durant le 1er sprint)
Marilyn Jacques-Sébastien
Lamine Lican

## Choix techniques :

Debian 12 est le système d'exploitation que nous allons utiliser pour notre serveur.
Les clients sont sous OS Windows 10 et ubuntu 22.04

## Difficultés rencontrées
Nous avons rencontré des difficultés lors du transfert des vm ubuntu et Windows 10 notamment à cause de la taille du fichier de la vm w10 
Nous avons eu des difficultés lors de l’installation de plex média server,differents problèmes dans le téléchargement.Pas toujours les bonnes versions de plex.Lorsque nous avons testé des commandes comme sudo apt install dirmngr ca-certificates software-properties-common apt-transport-https curl -y ou encore Sinon curl https://downloads.plex.tv/plex-keys/PlexSign.key | sudo apt-key add - cela en vain.La documentation de Plex n'était pas adaptée.

## Solutions/Alternatives trouvées :
Baudouin a alors décidé d’utiliser un autre compte pour pouvoir mettre la VMUbuntu sur un autre drive.Quand à la vm Windows nous avons utilise MEGA,qui est un service de stockage cloud dont les 20 premiers go sont gratuits.Nous avons alors décidé de tout reprendre à 0 et nous avons recherché une nouvelle documenation sur internet plus adapté à notre environnement de travail.Nous avons ainsi reussi l'installation de plex 

## Améliorations trouvées :
