<!--- STARTEXCLUDE --->
# 🎓 Cloner Netflix avec DataStax DB et GraphQL
[![KPLR](https://user-images.githubusercontent.com/123748165/226143592-ec837bc1-7879-41d9-816b-94ede52a7b82.png)](https://www.kplr.fr/qui-sommes-nous)
[![Gitpod ready-to-code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/from-referrer/)
[![License Apache2](https://img.shields.io/hexpm/l/plug.svg)](http://www.apache.org/licenses/LICENSE-2.0)



Un simple clone de page d'accueil **ReactJS** Netflix exécuté sur **DataStax DB** qui exploite l'API **GraphQL** avec *pagination* et *défilement infini*.
<!--- ENDEXCLUDE --->

Voir la présentation vidéo [Video Walkthrough](https://imgur.com/3ns3UJB) de ce que vous allez construire !

![image](https://github.com/yahia-kplr/workshop-graphql-netflix/blob/master/images/ui.png)

## 🎯  Objectifs
* Créez et exécutez un clone Netflix.
* Découvrez **l'API GraphQL** et comment l'utiliser avec une base de données pour créer les tables et parcourir les données.
* En savoir plus sur la **pagination** et le **défilement infini** dans une interface utilisateur Web.
* Tirez parti de Netlify et de DataStax Astra DB.
* Déployez le clone Netflix en production avec Netlify.

## Matériel pour la session

Peu importe que vous rejoigniez notre atelier en direct ou que vous préfériez le faire à votre rythme, nous avons ce qu'il vous faut. Dans ce référentiel, vous trouverez tout ce dont vous avez besoin pour cet atelier :

- [Slide deck](slides/slides.pdf)
- [Discord chat](https://bit.ly/cassandra-workshop)
- ["cassandra" sur StackOverflow](https://stackoverflow.com/questions/tagged/cassandra)
- ["cassandra" sur DBA StackExchange](https://dba.stackexchange.com/questions/tagged/cassandra)

# Commençons

## Table des matières

### Partie I - Configuration de la base de données et ingestion de données
1. [Créer une instance de base de données DataStax](#1-login-or-register-to-astradb-and-create-database)
2. [Créer un jeton de sécurité](#2-create-a-security-token)
3. [Créer une table pour les genres avec GraphQL](#3-create-table-for-genres-with-graphql)
4. [Insérer les données de genre avec GraphQL](#4-insert-genre-data-with-graphql)
5. [Récupérer les genres avec GraphQL](#5-retrieve-genres-with-graphql)
6. [Créer une table pour les films](#6-create-a-table-for-movies)
7. [Insérer quelques films](#7-insérer-quelques-films)
8. [Récupérer des films : pagination](#8-récupérer-films-pagination)

### Partie 2 – Créer et déployer le front-end

1. [Déployer l'interface graphique squelettique sur Netlify](#1-deploy-skeletal-gui-to-netlify)
2. [Lancez Gitpod depuis VOTRE dépôt Github](#2-launch-gitpod-from-your-github-repo)
3. [Configurer et utiliser `astra-cli`](#3-set-up-and-use-astra-cli)
4. [Fonctions sans serveur](#4-fonctions-sans-serveur)
5. [Récupération depuis le front-end](#5-fetching-from-the-front-end)
6. [Installer la CLI Netlify](#6-install-the-netlify-cli)
7. [Fournir les paramètres de connexion à la base de données](#7-provide-db-connection-parameters)
8. [Exécuter l'application en mode dev](#8-run-the-app-in-dev-mode)
9. [Connect to your Netlify site](#9-connect-to-your-netlify-site)
10. [Déployer en production !](#10-deploy-in-production)
