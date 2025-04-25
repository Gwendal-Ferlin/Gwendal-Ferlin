# Forum API - Symfony 6.4 & API Platform

![Symfony](https://img.shields.io/badge/Symfony-6.4-000000?style=for-the-badge&logo=symfony&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-8.1-777BB4?style=for-the-badge&logo=php&logoColor=white)
![API Platform](https://img.shields.io/badge/API_Platform-4.1-2A9FD8?style=for-the-badge&logo=api-platform&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-Authentication-000000?style=for-the-badge&logo=json-web-tokens&logoColor=white)

## 📋 Description

Ce projet est une API RESTful pour un système de forum développée avec Symfony 6.4 et API Platform. Elle permet la gestion des utilisateurs, des forums, et des messages avec authentification JWT.

## ✨ Fonctionnalités

- 🔐 **Authentification JWT** pour sécuriser l'accès à l'API
- 👥 **Gestion des utilisateurs** (inscription, connexion, profil)
- 📚 **Gestion des forums** (création, consultation, modification)
- 💬 **Gestion des messages** (publication, réponses, consultation)
- 🔍 **Filtrage et recherche** des messages et utilisateurs
- 📱 **API RESTful** complète avec documentation Swagger

## 🚀 Installation

### Prérequis

- PHP 8.1 ou supérieur
- Composer
- MySQL ou PostgreSQL
- Symfony CLI (optionnel)

### Étapes d'installation

1. **Cloner le repository**
   ```bash
   git clone https://github.com/votre-username/forum-api.git
   cd forum-api
   ```

2. **Installer les dépendances**
   ```bash
   composer install
   ```

3. **Configurer la base de données**
   - Copier le fichier `.env` en `.env.local`
   - Modifier les paramètres de connexion à la base de données

4. **Créer la base de données et exécuter les migrations**
   ```bash
   php bin/console doctrine:database:create
   php bin/console doctrine:migrations:migrate
   ```

5. **Charger les fixtures (optionnel)**
   ```bash
   php bin/console doctrine:fixtures:load
   ```

6. **Générer les clés JWT**
   ```bash
   php bin/console lexik:jwt:generate-keypair
   ```

7. **Lancer le serveur de développement**
   ```bash
   symfony server:start
   ```

## 📚 Documentation API

La documentation complète de l'API est disponible à l'adresse `/api/doc` une fois le serveur lancé.

### Points d'entrée principaux

- `POST /api/authentication_token` - Authentification JWT
- `GET /api/forums` - Liste des forums
- `GET /api/forums/{id}` - Détails d'un forum
- `GET /api/messages` - Liste des messages
- `GET /api/messages/{id}` - Détails d'un message
- `GET /api/users` - Liste des utilisateurs
- `GET /api/users/{id}` - Détails d'un utilisateur

## 🔒 Sécurité

- Authentification JWT pour toutes les routes protégées
- Validation des données avec Symfony Validator
- Protection CSRF
- Gestion des rôles utilisateurs

## 🛠️ Technologies utilisées

- **Symfony 6.4** - Framework PHP
- **API Platform** - Framework pour API RESTful
- **Doctrine ORM** - ORM pour la gestion de la base de données
- **LexikJWTAuthenticationBundle** - Authentification JWT
- **NelmioCorsBundle** - Gestion des CORS
- **Faker** - Génération de données de test

## 📝 Structure du projet

```
forum-api/
├── config/                 # Configuration Symfony
├── migrations/             # Migrations Doctrine
├── public/                 # Fichiers publics
├── src/                    # Code source
│   ├── Controller/         # Contrôleurs
│   ├── Entity/             # Entités Doctrine
│   ├── Repository/         # Repositories Doctrine
│   ├── State/              # Processeurs d'état API Platform
│   └── ...
├── templates/              # Templates Twig
├── tests/                  # Tests unitaires et fonctionnels
├── .env                    # Variables d'environnement
├── composer.json           # Dépendances PHP
└── README.md               # Documentation
```

## 🤝 Contribution

Les contributions sont les bienvenues ! N'hésitez pas à :

1. Fork le projet
2. Créer une branche pour votre fonctionnalité (`git checkout -b feature/AmazingFeature`)
3. Commiter vos changements (`git commit -m 'Add some AmazingFeature'`)
4. Pusher vers la branche (`git push origin feature/AmazingFeature`)
5. Ouvrir une Pull Request

## 📄 Licence

Ce projet est sous licence MIT. Voir le fichier `LICENSE` pour plus de détails.

## 👤 Auteur

Votre Nom - [@votre_twitter](https://twitter.com/votre_twitter) - email@example.com

---

<div align="center">
  <sub>Built with ❤️ using Symfony and API Platform</sub>
</div>
