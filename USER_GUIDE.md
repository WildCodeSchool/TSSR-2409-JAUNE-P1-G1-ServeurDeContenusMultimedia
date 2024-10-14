# Doc utilisateur : Installation et configuration de Plex sur un serveur Debian 12

## Les Prérequis matériels a avoir :
- Un PC Windows 10
- Un serveurs Debian 12
  
## Les Prérequis à avoir sur Windows 10 :
- Machine Renommé CLIWIN01
- Une adresse IP fixe
- Possède une connexion internet.

## Les Prérequis à avoir sur le serveur Debian 12 :
- Machine Renommé SRVLX01
- Une adresse IP fixe
- Possède une connexion internet.

## Partie 1 : Installation de plex

#### Nous salon Commencez par mettre à jour le serveur Debian 12 en fesant cette commande :
- sudo apt update && sudo apt upgrade

#### On va installer des paquets supplémentaires pour le bon fonctionnement du logiciel Plex :
- sudo apt install dirmngr ca-certificates software-properties-common apt-transport-https curl -y

#### On télécharge la clé Plex GPG, qui est utilisée pour vérifier l'authenticité des paquets :
- curl -fsSL https://downloads.plex.tv/plex-keys/PlexSign.key | gpg --dearmor | sudo tee /usr/share/keyrings/plex.gpg > /dev/null

  


## Utilisation de base :

## Utilisation avancée :

## FAQ :
