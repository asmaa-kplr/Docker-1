# Introduction à Docker Compose : Configuration d'une base de données PostgreSQL et de l'interface PgAdmin

Dans cet atelier, nous allons découvrir Docker Compose, un outil puissant pour gérer des applications multi-conteneurs. Nous allons apprendre comment configurer et exécuter une base de données PostgreSQL ainsi qu'une interface utilisateur PgAdmin, le tout dans des conteneurs isolés.

Nous allons créer un fichier docker-compose.yml dans lequel nous définirons les services PostgreSQL et PgAdmin. Le service PostgreSQL sera responsable de l'exécution de notre base de données PostgreSQL, tandis que le service PgAdmin fournira une interface web conviviale pour administrer et gérer la base de données.

## 1. Création du fichier docker_compose.yaml
```
services : 
  service1:
    .........
   service2:
    .........
```
## 2. Ajouter le service postgres
## 3. Specifier le nom du conteneur "container_name:.."
## 4. Indiquer l'image docker avec le tag ":latest" a partir du [Docker-Hub](https://hub.docker.com/_/postgres).
## 5. Définir les variables d'environement pour le conteneur PostgreSQL 
```
- POSTGRES_USER=${POSTGRES_USER}
- POSTGRES_PASSWORD=${POSTGRES_PW}
- POSTGRES_DB=${POSTGRES_DB}
```
