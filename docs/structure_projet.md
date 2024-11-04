# Structure du Projet FOFAL ERP

## Organisation des Dossiers

```
fofal_erp_2024/
├── backend/
│   ├── alembic/          # Migrations de base de données
│   ├── app/
│   │   ├── core/         # Configuration et utilitaires core
│   │   ├── models/       # Modèles de données
│   │   ├── schemas/      # Schémas Pydantic (à implémenter)
│   │   ├── api/          # Endpoints API (à implémenter)
│   │   └── services/     # Logique métier (à implémenter)
│   └── tests/            # Tests unitaires (à implémenter)
│
├── frontend/             # Application React (à créer)
│   ├── src/
│   │   ├── components/   # Composants React
│   │   ├── pages/        # Pages de l'application
│   │   ├── services/     # Services API
│   │   └── utils/        # Utilitaires
│   └── tests/           # Tests frontend
│
├── docs/                # Documentation
│   ├── api_reference.md
│   ├── guide_installation.md
│   ├── configuration_base_donnees.md
│   └── ...
│
└── config/             # Configuration globale
```

## Composants Principaux

### Backend

1. **Core (/backend/app/core/)**
   - Configuration de base de données
   - Gestion des authentifications
   - Middlewares

2. **Models (/backend/app/models/)**
   - Modèles SQLAlchemy
   - Relations entre modèles
   - Validation des données

3. **API (à implémenter)**
   - Endpoints REST
   - Validation des requêtes
   - Gestion des erreurs

### Frontend (à créer)

1. **Components**
   - Composants réutilisables
   - Formulaires
   - Tables et listes

2. **Pages**
   - Dashboard
   - Gestion des parcelles
   - Suivi des récoltes
   - Gestion des stocks

3. **Services**
   - Intégration API
   - Gestion d'état
   - Authentification

## Prochaines Étapes

1. **Backend**
   - Implémenter les endpoints API
   - Ajouter les tests unitaires
   - Configurer l'authentification

2. **Frontend**
   - Initialiser le projet React
   - Créer les composants de base
   - Intégrer avec l'API

3. **DevOps**
   - Configurer Docker
   - Mettre en place CI/CD
   - Préparer les environnements
