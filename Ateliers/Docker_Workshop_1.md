# Commandes de base de Docker

Cet exercice vous a permis de pratiquer les commandes de base de Docker, y compris : 

* La vérification de la version de Docker
* L'affichage des conteneurs en cours d'exécution 
* La gestion des images Docker
* Le téléchargement d'une image depuis un registre
* La suppression d'une image de votre machine.
  
******************************************************************************************************************************************************************
### Créer un nouveau repository Github Vide

Connectez-vous à votre compte GitHub et cliquez sur le bouton "New" pour créer un nouveau dépôt. Donnez un nom et une description au dépôt et choisissez les options appropriées, telles que la visibilité et le fichier README.md. Cliquez sur le bouton "Create repository" pour créer le nouveau dépôt.

![image](https://user-images.githubusercontent.com/123757632/221904279-c5a2d920-5b45-4193-b599-1cc21daae210.png)

### Ouvrir le dépot Github directement sur Gitpod

Etapes pour création et utilisation de [Gitpod](https://github.com/kplr-training/Git-Github/blob/main/Ateliers/Gitpod%20101.md).

******************************************************************************************************************************************************************

## 1. Afficher la version de Docker installée

La commande docker --version est utilisée pour afficher la version de Docker installée sur votre système. Lorsque vous exécutez cette commande, elle affiche la version de Docker suivie du numéro de version.

```
 docker ********
```
Voici un exemple de sortie possible :

```
Docker version 20.10.7, build f0df350
```

Dans cet exemple, la version de Docker installée est "20.10.7" avec le numéro de build "f0df350". Cette information est utile pour vérifier la version de Docker que vous utilisez et pour vous assurer que votre environnement est correctement configuré.

## 2. Afficher la liste des conteneurs en cours d'exécution.

```
$ docker ********
```
La commande `docker ********` est utilisée pour afficher les conteneurs Docker en cours d'exécution sur votre système. Elle affiche une liste des conteneurs actifs avec des détails tels que l'ID du conteneur, l'image utilisée, le nom du conteneur, le statut, les ports exposés, et d'autres informations.

Lorsque vous exécutez la commande `docker ps` sans aucun argument supplémentaire, elle affiche uniquement les conteneurs en cours d'exécution.

Voici un exemple de sortie possible :

```
CONTAINER ID   IMAGE              COMMAND                  CREATED         STATUS         PORTS                  NAMES
```

## 3. Afficher la liste des images Docker disponibles sur votre machine. 

```
$ docker ********
```

La commande `docker ********` est utilisée pour afficher la liste des images Docker présentes sur votre système. Elle affiche les détails des images telles que le nom de l'image, le tag, l'ID de l'image, la taille de l'image et la date de création.

Voici un exemple de sortie possible :

```
REPOSITORY          TAG       IMAGE ID       CREATED         SIZE
```
La commande `docker ********` vous permet de visualiser les images Docker disponibles sur votre système, ce qui peut être utile pour gérer et vérifier les images que vous utilisez pour vos conteneurs.

## 4. Télécharger l'image "hello-world" depuis le Docker Hub.

```
$ docker ******** hello-world
```

La commande docker ******** hello-world est utilisée pour télécharger l'image Docker "hello-world" à partir du registre Docker Hub sur votre système local. L'image "hello-world" est un exemple minimaliste utilisé couramment pour vérifier que l'installation de Docker fonctionne correctement.

Lorsque vous exécutez la commande docker ******** hello-world, Docker va chercher l'image "hello-world" sur Docker Hub (si elle n'est pas déjà présente sur votre système) et la télécharge localement.

## 5. Vérifiez à nouveau les images Docker disponibles.

```
$ docker ********
```
Après avoir exécuté la commande `docker pull hello-world` et téléchargé l'image "hello-world" à partir de Docker Hub, vous pouvez utiliser la commande `docker ********` pour afficher la liste des images Docker présentes sur votre système.

Voici un exemple de sortie possible après avoir téléchargé l'image "hello-world" :

```
REPOSITORY          TAG       IMAGE ID       CREATED         SIZE
hello-world         latest    abcdef123456   1 minute ago    4.85kB
```

Dans cet exemple, l'image "hello-world" est répertoriée avec le tag "latest". L'ID de l'image est "abcdef123456" et la taille est de 4.85kB. Cela indique que l'image "hello-world" a été téléchargée avec succès et est maintenant disponible sur votre système.

Vous pouvez utiliser cette image pour créer un conteneur Docker en utilisant la commande `docker run hello-world` et vérifier le bon fonctionnement de votre installation Docker.

## 6. Créer un conteneur Docker pour utiliser l'image hello-world

```
$ docker ******** hello-world
```
La commande `docker ******** hello-world` est utilisée pour exécuter un conteneur Docker basé sur l'image "hello-world". Cette image est généralement utilisée à des fins de test et de vérification de l'installation de Docker.

Lorsque vous exécutez cette commande, Docker va chercher l'image "hello-world" sur votre système (ou la télécharger automatiquement depuis Docker Hub si elle n'est pas présente localement), puis il va créer et lancer un conteneur basé sur cette image.

Le conteneur "hello-world" affichera un message simple pour confirmer que Docker fonctionne correctement. Voici un exemple de sortie possible :

```
Hello from Docker!
This message shows that your installation appears to be working correctly.
...
```

Si vous voyez ce message, cela signifie que Docker est correctement installé et opérationnel sur votre système.

Après l'exécution du conteneur "hello-world", il se terminera automatiquement et n'aura pas d'impact persistant sur votre système.

## 7. Vérifier la list des conteneurs 

```
$ docker ********
```
La commande `docker ********` est utilisée pour afficher tous les conteneurs Docker présents sur votre système, qu'ils soient en cours d'exécution ou arrêtés. Elle affiche une liste complète des conteneurs avec des détails tels que l'ID du conteneur, l'image utilisée, le nom du conteneur, le statut, les ports exposés, et d'autres informations.

Lorsque vous exécutez la commande `docker ********`, elle affiche tous les conteneurs, y compris ceux qui sont arrêtés.

Voici un exemple de sortie possible :

```
CONTAINER ID   IMAGE              COMMAND                  CREATED           STATUS                     PORTS                  NAMES
f1e3d9fe4c5a   hello-world        "/hello"                 2 minutes ago     Exited (0) 2 minutes ago                          vibrant_khayyam
```

## 8. Supprimer le conteneur de l'image hello-world

```
$ docker ******** <ID_conteneur>
```
Après avoir exécuté la commande docker******** <ID_conteneur>, Docker supprimera le conteneur spécifié de votre système si celui-ci existe. Vous pouvez utiliser la commande docker ps -a pour vérifier que le conteneur a été supprimé avec succès.

## 9. Vérifier la list des conteneurs 

La commande `docker ********` vous permet de voir tous les conteneurs présents sur votre système, qu'ils soient actifs ou arrêtés, ce qui peut être utile pour gérer et inspecter l'historique des conteneurs.

```
$ docker ********
```

Le but de l'utilisation de cette commande est de vérifier que le conteneur de l'image est supprimé


## 10. Supprimer l'image "hello-world" de votre machine.

```
$ docker ******** hello-world
```

La commande docker ******** hello-world est utilisée pour supprimer une image Docker de votre système. En utilisant cette commande avec l'argument hello-world, vous indiquez à Docker de supprimer l'image "hello-world" de votre système local.

Après avoir exécuté la commande docker ******** hello-world, Docker supprimera l'image "hello-world" de votre système si elle est présente. Vous pouvez utiliser la commande docker images pour vérifier que l'image "hello-world" a été supprimée avec succès.

## 11. Vérifiez à nouveau les images Docker disponibles.

```
$ docker ********
```

Le but de l'utilisation de cette commande est de vérifier que l'image est supprimé

