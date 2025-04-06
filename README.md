# Project: Application Fullstack avecDicker et Postgres, Redis ainsi que Nginx

Le projet docker suivant est un projet qui comporte certaines solutions d'exercices des cours que l'on peut retrouver sur https://devopswithdocker.com/.
Il comporte une app front-end, en React, on peut faire une requête sur le port 5000, le backend a été fait en Go, les connections sont faites sur le port 8080.
Il y a une base de données en postgresql ainsi que l'utilisation de redis pour se connecter au backend. 
Il y a en outre Nginx fonctionne comme un proxy inverse. Les requêtes arrivant sur autre chose que /api seront redirigées vers le conteneur frontend et /api sera redirigé vers le conteneur backend. 
Pour conclure, le frontend est accessible simplement en allant sur http://localhost.


## Il y a des etapes pour faire fonctionner le projet


- Assurez-vous que le moteur docker est installé dans le système ; consultez la documentation officielle : [https://docs.docker.com/engine/install/]
- Installez également docker-compose dans le système ; consultez la documentation officielle : [https://docs.docker.com/compose/install/]
- Exécutez avec Docker Compose

  ```console
  $ docker-compose up -d
  $ docker-compose ps
  # Pour arrêter les containers
  $ docker-compose down
  ```

- Pour voir le frontend: http://localhost

## Features

- Frontend écrit en React
- Backend écrit en Go
- Base de données PostgreSQL connectée au Backend
- Base de données en mémoire Redis connectée au Backend
- Nginx comme Proxy Inverse

## Les exercices qui ont été faits :

- 1.12 : Création d’un Dockerfile pour le frontend (port 5000)
- 1.13 : Création d’un Dockerfile pour le backend (port 8080)
- 1.14 : Configuration des ports pour permettre la communication entre frontend et backend via le navigateur
- 2.3 : Intégration du frontend et backend dans docker-compose
- 2.4 : Connexion de Redis au backend via le réseau Docker
- 2.6 : Ajout de PostgreSQL et configuration avec le backend
- 2.8 : Mise en place de Nginx comme reverse proxy redirigeant /api vers le backend et le reste vers le frontend
- 2.9 / 2.10 : Lancement complet de l’application avec docker-compose up, tous les services sont fonctionnels
- 3.3 : Exécution des conteneurs avec un utilisateur non-root pour plus de sécurité
- 3.4 / 3.5 : Optimisation de la taille des images Docker
- 3.6 : Mise en place d’un build multi-étapes pour l’application backend

