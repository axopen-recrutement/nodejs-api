# Épreuve recrutement Axopen NodeJS / Express

Cette application est utilisée comme exercice de recrutement pour AXOPEN. Il ne représente en rien le niveau de qualité des développements d'AXOPEN.

## Qu'est ce que je dois faire ?

Dans cet exercice, il vous est demandé dans un premier temps, de relire le code et de le comprendre. 
Par la suite, l'objectif est de nous faire un retour sur la qualité du code ainsi qu'une liste des améliorations que vous pourriez apporter à l'application.

Les types de retour peuvent être liés à différentes thématiques, voici une liste non-exhaustive :
- Structure de l'application
- Syntaxe
- Logique
- Lisibilité
- Performance
- Bonnes pratiques


Une fois ces étapes effectuées, vous pouvez nous envoyer votre rapport sous différents formats : 
- Markdown
- Word
- Fichier texte

## Comment lancer l'application ?

> Note : Il n'est pas primordial de lancer l'application pour effectuer l'analyse de code.

Cette application est fonctionnelle, et ne demande qu'une base de données MariaDB afin de pouvoir être lancée.
Vous pouvez, si vous le souhaitez, lancer l'application après avoir installé la BDD et créer les tables tels que définis dans `db.sql`.
Pour que votre application se connecte à la BDD, vous devez renseigner les informations de connexion dans le fichier `utils/database-connection.js`.

## Que contient l'application ?

Il s'agit d'une API REST, qui permet les interactions suivantes :
- Créer un utilisateur
- Se connecter grâce à un utilisateur existant, afin de récupérer un token
- Créer un `chantier` avec des informations aléatoires
- Modifier un chantier
- Récupérer un chantier
- Supprimer un chantier

Toutes les routes concernant les chantiers sont protégées, et demandes un token de type `Bearer` (obtenu grâce à la connexion).

### Architecture du projet 

Nous allons détailler rapidement ce qui se trouve dans chaque dossier.

- `utils` contient un ensemble de fichiers triés par thématique avec un ensemble de fonctions réutilisable dans l'application.
- `api/helpers` contient les actions associées aux différents endpoints API
- `api/routes` contient la définition des routes HTTP de l'API.
- `api/index.js` ce fichier est le fichier root de l'API et contient la configuration de l'API. 