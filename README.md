# TSSR-2409-JAUNE-P1-G1-ServeurDeContenusMultimedia

## Présentation du projet
L'**objectif principal** du projet est de créer un serveur et d'y installer un service qui agira comme une palteforme centralisée pour stocker, organiser et diffuser divers types de médias.
L'**objectif secondaire** est de mettre en place la configuration avancée des bibliothèques de médias et des métadonnées. Ce projet pourra servir dans le futur comme base, pour faire fonctionner un serveur NAS dedié à la gestion de fichiers multimédias. 

## Introduction : 
Dans un monde où la consommation de contenus multimédias ne cesse d’augmenter, il devient essentiel pour les entreprises et les particuliers de disposer d'une solution centralisée pour gérer leurs médias numériques. Ce projet répond à ce besoin en proposant une plateforme flexible et performante, capable de s'adapter à différents environnements et besoins.

## Membres du groupe :
Baudouin Soubrier De Gaudemar (Product Master durant le 1er sprint)
Erwan Salomon (Scrum Master durant le 1er sprint)
Marilyn Jacques-Sébastien (Scrum Master durant le 2ème sprint)
Lamine Lican (Product Owner durant le 2ème sprint) 

## Choix techniques :

Le projet a deux impératifs techniques. La VM serveur doit fonctionner sous [Debian 12](https://www.debian.org/) et le logiciel de gestion de contenus doit être [Plex](https://www.plex.tv/). Pour nos VMs clients, nous pouvons utiliser tous les OS.
Nous avons donc privilégié les OS [Windows 10](https://www.microsoft.com/fr-fr/software-download/windows10%20) et [Ubuntu 24.04 LTS](https://ubuntu.com/blog/tag/ubuntu-24-04-lts), qui sont les OS que nous avons le plus utilisé lors de notre début de formation.
Chaque VM devait suivre une pré-configuration précise détaillée dans le tableau ci-dessous :
|     OS       |    Nom   |            Compte           |    Mdp   |    Adresse IP   |
|:------------:|:--------:|:---------------------------:|:--------:|:---------------:|
|   Debian 12  |  SRVLX01 |             root            | Azerty1* | 172.16.10.10/24 |
| Ubuntu 24.04 | CLILIN01 |     wilder (groupe sudo)    | Azerty1* | 172.16.10.20/24 |
|  Windows 10  | CLIWIN02 | wilder (groupe admin local) | Azerty1* | 172.16.10.30/24 |


## Difficultés rencontrées

Malgré une nouvelle méthodologie de travail de groupe, nous avons su nous adapter rapidement, ce qui nous a grandement aidé pour le reste des sprints. Cependant, le premier projet en groupe, nous a confronté de nombreuses fois à des soucis sur le plan technique. Tout d'abord un premier problème logistique pour exporter des VMs configurées par Baudouin; lié à un manque d'information de notre part. Puis, lors de l'installation du service Plex Media Server, nous avons fait face à 3 problèmes majeurs.

### La documentation Plex
Dans un soucis de vouloir faire les choses correctement, nous nous sommes basés sur la documentation de Plex pour son installation sur notre serveur Deabian. Les plusieurs dizaines d'articles présents dans la catégories Plex Media Server, et un suivi scrupulueux des étapes d'installation nous ne parvenions pas à installer le service. Après plusieurs essais et approches différentes via la documentation officielle, nous avons cherché d'autres sources afin de réussir.
Cela nous a fait perdre plusieurs heures précieuses et cela nous a obligé à recommencer sur une VM Debian de zéro.


### VM Serveur & Déconnexions

### ?? 


Nous avons rencontré des difficultés lors du transfert des vm ubuntu et Windows 10 notamment à cause de la taille du fichier de la vm w10 
Nous avons eu des difficultés lors de l’installation de plex média server,differents problèmes dans le téléchargement.Pas toujours les bonnes versions de plex.Lorsque nous avons testé des commandes comme sudo apt install dirmngr ca-certificates software-properties-common apt-transport-https curl -y ou encore Sinon curl https://downloads.plex.tv/plex-keys/PlexSign.key | sudo apt-key add - cela en vain.La documentation de Plex n'était pas adaptée.

## Solutions/Alternatives trouvées :
Baudouin a alors décidé d’utiliser un autre compte pour pouvoir mettre la VMUbuntu sur un autre drive.Quand à la vm Windows nous avons utilise MEGA,qui est un service de stockage cloud dont les 20 premiers go sont gratuits.Nous avons alors décidé de tout reprendre à 0 et nous avons recherché une nouvelle documenation sur internet plus adapté à notre environnement de travail.Nous avons ainsi reussi l'installation de plex 

## Améliorations trouvées :
