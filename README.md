# Projet-serveur-web
Cette application permet de gérer les informations académiques, y compris les étudiants, les enseignants, les matières, les notes et les évaluations. Elle vise à faciliter le suivi des performances des étudiants en centralisant toutes les informations de cours.

## Fonctionnalités

- **Gestion des étudiants** : Ajout, mise à jour, suppression et consultation des informations des étudiants.
- **Gestion des enseignants** : Suivi des enseignants et de leurs matières enseignées.
- **Gestion des matières** : Création de matières, incluant le nom, la description, et le coefficient.
- **Gestion des notes** : Saisie et gestion des notes pour chaque étudiant par matière et enseignant.
- **Classes et évaluations** : Association des étudiants aux classes et suivi des évaluations.

## Structure de la Base de Données

1. **Students (Étudiants)**
   - `id`, `nom`, `prénom`, `date_de_naissance`, `adresse`, `téléphone`, `email`

2. **Teachers (Enseignants)**
   - `id`, `nom`, `prénom`, `adresse`, `téléphone`, `email`, `matière_enseignée`

3. **Subjects (Matières)**
   - `id`, `nom`, `description`, `coefficient`

4. **Grades (Notes)**
   - `id`, `id_étudiant`, `id_matière`, `id_enseignant`, `note`, `date_d'évaluation`

5. **Classes**
   - `id`, `nom`, `niveau`, `id_enseignant`

6. **Assessments (Évaluations)**
   - `id`, `id_matière`, `id_classe`, `date_d'évaluation`, `type_d'évaluation`

## Technologies Utilisées

- **Backend** : Node.js, Express.js
- **Base de données** : MySQL avec Sequelize ORM
- **Frontend** (à venir) : Vue.js

## Installation

1. Cloner le dépôt :

    ```bash
    git clone https://github.com/yourusername/gestion-notes-cours.git
    cd gestion-notes-cours
    ```

2. Installer les dépendances :

    ```bash
    npm install
    ```

3. Configurer les variables d'environnement en créant un fichier `.env` :

    ```
    DB_USERNAME=root
    DB_PASSWORD=your_password
    DB_DATABASE=gestion_notes
    DB_HOST=127.0.0.1
    ```

4. Lancer les migrations Sequelize pour créer la base de données :

    ```bash
    npx sequelize db:migrate
    ```

5. Démarrer l'application :

    ```bash
    npm start
    ```

## Fonctionnalités à venir

- Interface utilisateur pour gérer les données académiques
- Rapports et analyses des performances des étudiants

## Licence

Ce projet n'a pas de licence.
