# Documentation API FOFAL ERP

## Base URL
```
http://localhost:8000/api/v1
```

## Authentification
L'API utilise JWT (JSON Web Tokens) pour l'authentification.

### Obtenir un token
```http
POST /auth/token
Content-Type: application/json

{
    "username": "string",
    "password": "string"
}
```

## Endpoints

### 1. Module Production

#### Parcelles
- GET /parcelles - Liste des parcelles
- POST /parcelles - Créer une parcelle
- GET /parcelles/{id} - Détails d'une parcelle
- PUT /parcelles/{id} - Modifier une parcelle

#### Récoltes
- POST /recoltes - Enregistrer une récolte
- GET /recoltes - Liste des récoltes
- GET /recoltes/{id} - Détails d'une récolte

### 2. Module Inventaire

#### Produits
- GET /produits - Liste des produits
- POST /produits - Ajouter un produit
- PUT /produits/{id} - Modifier un produit

#### Stock
- POST /stock/mouvements - Enregistrer un mouvement
- GET /stock/etat - État du stock

### 3. Module Finance

#### Transactions
- POST /transactions - Créer une transaction
- GET /transactions - Liste des transactions
- PUT /transactions/{id}/valider - Valider une transaction

### 4. Module RH

#### Employés
- GET /employes - Liste des employés
- POST /employes - Ajouter un employé
- PUT /employes/{id} - Modifier un employé

#### Présences
- POST /presences - Enregistrer une présence
- GET /presences - Liste des présences

## Pagination
```
GET /endpoint?page=1&limit=10
```

## Filtrage
```
GET /parcelles?culture_type=PALMIER&statut=ACTIVE
```

## Codes d'Erreur
- 400: Requête invalide
- 401: Non authentifié
- 403: Non autorisé
- 404: Ressource non trouvée
- 422: Erreur de validation
- 500: Erreur serveur
