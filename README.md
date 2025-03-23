# DevNetwork
# Cahier des Charges pour le Projet DevNetwork



## 1. Contexte et Définition du Projet
Le projet **DevNetwork** est une plateforme web destinée aux développeurs pour partager leurs projets, collaborer, évaluer le travail des autres et rechercher des profils de développeurs. Actuellement, les développeurs manquent d'une plateforme centralisée pour partager leurs réalisations, échanger des idées et établir des connexions professionnelles. DevNetwork vise à combler ce besoin en offrant un espace interactif et collaboratif.

### Problématique :
- **Manque de visibilité** pour les projets personnels des développeurs.
- **Difficulté à trouver des collaborateurs ou des mentors**.
- **Absence d'un système unifié** pour évaluer et commenter le travail des autres développeurs.

### Contraintes :
- Utilisation de **Django** comme framework principal.
- Intégration d'une base de données **PostgreSQL** pour la gestion des données.
- Déploiement sur une plateforme **cloud** pour une accessibilité mondiale.



## 2. Objectifs
Les objectifs du projet sont les suivants :
1. **Créer une plateforme centralisée** pour les développeurs afin de partager leurs projets et collaborer.
2. **Faciliter la recherche** de profils de développeurs en fonction de leurs compétences et projets.
3. **Permettre l'évaluation et le feedback** sur les projets partagés.
4. **Offrir un système de messagerie** pour permettre aux utilisateurs de communiquer entre eux.
5. **Atteindre un taux d'utilisation de 70%** parmi les développeurs inscrits dans les 6 premiers mois après le lancement.



## 3. Périmètre
Le périmètre du projet inclut :
- **Cible** : Développeurs web et logiciels, qu'ils soient débutants ou expérimentés.
- **Plateforme** : Application web responsive, accessible via navigateur.
- **Fonctionnalités principales** :
  - Partage de projets.
  - Recherche de développeurs.
  - Système de notation et de commentaires.
  - Messagerie interne.
- **Exclusions** :
  - Développement d'une application mobile native.
  - Intégration de fonctionnalités de paiement ou de monétisation.



## 4. Parties Prenantes
Les parties prenantes du projet sont :
1. **Développeurs** : Utilisateurs principaux de la plateforme.
2. **Équipe de développement** : Responsable de la conception, du développement et de la maintenance de la plateforme.
3. **Mentors et formateurs** : Utilisateurs avancés qui peuvent guider les débutants.
4. **Administrateurs** : Gestionnaires de la plateforme, responsables de la modération et de la maintenance.
5. **Investisseurs** : Parties intéressées par le succès et la croissance de la plateforme.



## 5. Description des Besoins

### 5.1. Besoins Fonctionnels
| **Objectif**                     | **Description**                                                                 | **Contraintes/Règles de Gestion**                     | **Priorité** |
|----------------------------------|---------------------------------------------------------------------------------|-------------------------------------------------------|--------------|
| **Inscription et Authentification** | Permettre aux utilisateurs de créer un compte et de se connecter.               | Utilisation de Django REST Framework pour l'API.      | Haute        |
| **Partage de Projets**           | Les utilisateurs peuvent publier leurs projets avec des descriptions et des tags.| Limite de 5 projets par utilisateur.                  | Haute        |
| **Recherche de Développeurs**    | Les utilisateurs peuvent rechercher des profils par compétences ou projets.     | Recherche full-text avec PostgreSQL.                  | Haute        |
| **Système de Notation**          | Les utilisateurs peuvent noter et commenter les projets des autres.             | Notation sur 5 étoiles avec commentaires optionnels.  | Moyenne      |
| **Messagerie Interne**           | Les utilisateurs peuvent envoyer des messages privés à d'autres utilisateurs.   | Limite de 10 messages non lus par utilisateur.        | Moyenne      |
| **Gestion des Profils**          | Les utilisateurs peuvent mettre à jour leurs informations et compétences.       | Validation des compétences par l'administrateur.      | Haute        |

### 5.2. Besoins Non Fonctionnels
| **Objectif**                     | **Description**                                                                 | **Contraintes/Règles de Gestion**                     | **Priorité** |
|----------------------------------|---------------------------------------------------------------------------------|-------------------------------------------------------|--------------|
| **Performance**                  | Temps de réponse de la plateforme inférieur à 2 secondes.                       | Utilisation de Whitenoise pour les fichiers statiques.| Haute        |
| **Sécurité**                     | Protection des données utilisateurs et des transactions.                        | Utilisation de Django REST Framework SimpleJWT.       | Haute        |
| **Scalabilité**                  | La plateforme doit supporter jusqu'à 10 000 utilisateurs simultanés.            | Déploiement sur une infrastructure cloud scalable.    | Moyenne      |
| **Compatibilité**                | Compatibilité avec les navigateurs modernes (Chrome, Firefox, Safari, Edge).    | Tests cross-browser obligatoires.                     | Haute        |
| **Disponibilité**                | Taux de disponibilité de 99,9%.                                                | Utilisation de Gunicorn pour le déploiement.          | Haute        |
