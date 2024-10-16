# Doc admin

## Pré-requis techniques
- Virtualbox
- Os serveur Debian 
- OS client Ubuntu 24.04
- OS client Windows 10

# Configuration du serveur Debian 12

### Visualiser la configuration réseau actuelle :

Afficher la configuration réseau actuel de la machine.
-	ip a
  
Puis trouver l'interface correspondante à la carte réseau connectée au réseau local. 

### Définir une adresse IP fixe :
Nous allons éditer le fichier de la carte réseau
-	sudo nano /etc/network/interfaces


# **Doc Admin installation de Plex sur Debian 12**
 
## **Mettre à jour le système Debian avant l'installation de Plex**
 
Commencez par mettre à jour votre système Debian afin d'assurer un processus d'installation fluide. Cela permet de s'assurer que tous les paquets existants sont à jour :
 
> **sudo apt update && sudo apt upgrade**
 
## **Installer les paquets requis pour Plex**
 
L'installation de Plex nécessite des paquets supplémentaires. Installez-les en exécutant la commande suivante :
 
> **sudo apt install dirmngr ca-certificates software-properties-common apt-transport-https curl -y**
 
Ces paquets fournissent les outils nécessaires pour gérer le dépôt Plex, notamment les connexions sécurisées et la gestion des clés GPG.
 
## **Ajouter le dépôt APT de Plex**
 
Ajoutez le dépôt Plex à votre système Debian pour installer Plex depuis la source officielle. Cela vous permet d'installer et de mettre à jour le logiciel directement à partir du dépôt officiel en utilisant le gestionnaire de paquets APT.
 
Tout d'abord, ouvrez votre terminal et importez la clé GPG de Plex avec la commande suivante :
 
> **curl -fsSL [https://downloads.plex.tv/plex-keys/PlexSign.key](https://downloads.plex.tv/plex-keys/PlexSign.key) | gpg --dearmor | sudo tee /usr/share/keyrings/plex.gpg > /dev/null**
 
Cette commande **télécharge et convertit la clé GPG de Plex**, qui est utilisée pour vérifier l'authenticité des paquets provenant du dépôt.
 
Ensuite, ajoutez le dépôt Plex à votre système :
 
> **echo "deb [signed-by=/usr/share/keyrings/plex.gpg] [https://downloads.plex.tv/repo/deb](https://downloads.plex.tv/repo/deb) public main" | sudo tee /etc/apt/sources.list.d/plexmediaserver.list**
 
Cette commande **crée un nouveau fichier dans le répertoire sources.list.d** avec les informations nécessaires pour accéder au dépôt Plex.
 
## **Installer Plex Media Server via APT**
 
Avant d'installer Plex, mettez à jour l'index des paquets pour inclure le nouveau dépôt Plex que vous venez d'ajouter :
 
> **sudo apt update**
 
Vous pouvez maintenant installer Plex Media Server sur Debian avec la commande suivante :
 
> **sudo apt install plexmediaserver**
 
Pendant l'installation, une invite peut vous demander si vous souhaitez remplacer la liste des référentiels. Tapez **«N»** pour continuer l'installation, car la clé GPG signée correcte est déjà en place.
 
## **Vérifier l'installation de Plex Media Server**
 
Par défaut, le service Plex Media Server devrait démarrer automatiquement. Pour vérifier cela, utilisez la commande suivante pour afficher l'état du service :
 
> **systemctl status plexmediaserver**


![Serveur actif](./IMAGES/serverOk.png)


----------
