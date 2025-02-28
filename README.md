<!--- STARTEXCLUDE --->
# 🎓 Cloner Netflix avec DataStax DB et GraphQL
[![KPLR](https://user-images.githubusercontent.com/123748165/226143592-ec837bc1-7879-41d9-816b-94ede52a7b82.png)](https://www.kplr.fr/qui-sommes-nous)
[![Gitpod ready-to-code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/from-referrer/)
[![License Apache2](https://img.shields.io/hexpm/l/plug.svg)](http://www.apache.org/licenses/LICENSE-2.0)



Un simple clone de page d'accueil **ReactJS** Netflix exécuté sur **DataStax DB** qui exploite l'API **GraphQL** avec *pagination* et *défilement infini*.
<!--- ENDEXCLUDE --->

Voir la présentation vidéo [Resultat Final](https://glittery-twilight-7ada8e.netlify.app/) de ce que vous allez construire !

![🎓Cloner Netflix avec Datastax et GraphQL](https://user-images.githubusercontent.com/123748165/226187624-3012341b-d74a-41a5-8a5b-181121091157.png)

## 🎯  Objectifs
* Créez et exécutez un clone Netflix.
* Découvrez **l'API GraphQL** et comment l'utiliser avec une base de données pour créer les tables et parcourir les données.
* En savoir plus sur la **pagination** et le **défilement infini** dans une interface utilisateur Web.
* Tirez parti de Netlify et de DataStax Astra DB.
* Déployez le clone Netflix en production avec Netlify.

<details><summary>C'est quoi Graphql</summary>
GraphQL est un langage de requête de données open source développé par Facebook en 2012 pour simplifier la communication entre les applications frontales et les serveurs de données. Contrairement aux API REST traditionnelles, GraphQL permet aux clients de spécifier précisément les données dont ils ont besoin, ce qui évite le surchargement de l'API avec des requêtes multiples et redondantes.

Avec GraphQL, les clients peuvent interroger une API pour récupérer uniquement les données nécessaires à leur application, ce qui peut réduire considérablement la quantité de données transférées et améliorer les performances. GraphQL fournit également une documentation complète pour l'API, ce qui facilite la compréhension et l'utilisation de l'API par les développeurs.

En somme, GraphQL est un langage de requête flexible et efficace pour les API qui permet aux clients de spécifier exactement les données dont ils ont besoin, en évitant le gaspillage de ressources et en améliorant les performances.

</details>

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

