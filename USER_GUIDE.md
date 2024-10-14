# Doc utilisateur : Installation de Plex sur un serveur Debian 12

### Les Prérequis matériels a avoir :
- Un PC Windows 10 ou un PC Ubuntu (Linux)
- Un serveurs Debian 12 (Linux)
  
### Les Prérequis à avoir sur Windows 10, Ubuntu et le serveur Debian 12 :
- Une adresse IP fixe
- Possède une connexion internet.

## Étape 1 : Installation de plex

#### Avant de commencer, nous allons voir si vous savez bien Internet. 
- ping 8.8.8.8

#### Nous allons Commencez par mettre à jour le serveur Debian 12 en fesant cette commande :
- sudo apt update && sudo apt upgrade

#### On va installer des paquets supplémentaires pour le bon fonctionnement du logiciel Plex :
- sudo apt install dirmngr ca-certificates software-properties-common apt-transport-https curl -y

#### On télécharge la clé Plex GPG, qui est utilisée pour vérifier l'authenticité des paquets :
- curl -fsSL https://downloads.plex.tv/plex-keys/PlexSign.key | gpg --dearmor | sudo tee /usr/share/keyrings/plex.gpg > /dev/null

#### On crée un nouveau fichier dans le sources.list.d répertoire avec les informations nécessaires sur le référentiel Plex.
- echo "deb [signed-by=/usr/share/keyrings/plex.gpg] https://downloads.plex.tv/repo/deb public main" | sudo tee /etc/apt/sources.list.d/plexmediaserver.list

#### Avant d'installer Plex, on va mettez à jour l'index du paquet pour inclure le référentiel Plex nouvellement ajouté :
- sudo apt update
  
#### Installation du logiciel Plex :
- sudo apt install plexmediaserver

#### Avec cette commande, nous salon vérifier que le service Plex et bien démarrer (Normalement le service Plex doit démarrer automatiquement).
- systemctl status plexmediaserver

#### Vous venez de terminer l'installation de votre serveur multimédia.
#### Si vous rencontrez des problèmes pendant l'installation, merci de vous référer à la FAQ en bas de la page.

 ## Étape 2 : Accéder à l’interface Web sur votre ordinateur
 


## Utilisation de base :


## Utilisation avancée :


## FAQ :
#### Que faire si je n’ai pas Internet ?

#### Que faire si le service Plex Media Server n’ais pas actif ?

#### Si le service n'est pas actif, utilisez la commande suivante pour démarrer Plex Media Server :

- sudo systemctl start plexmediaserver


