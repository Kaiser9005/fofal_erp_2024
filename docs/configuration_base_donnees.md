# Configuration de la Base de Données FOFAL ERP

## PostgreSQL

### Installation

1. Installation de PostgreSQL
```bash
sudo apt update
sudo apt install postgresql postgresql-contrib
```

2. Démarrage du service
```bash
sudo systemctl start postgresql
sudo systemctl enable postgresql
```

### Configuration

1. Création de la base de données
```sql
CREATE DATABASE fofal_erp;
CREATE USER fofal_user WITH PASSWORD 'votre_mot_de_passe';
GRANT ALL PRIVILEGES ON DATABASE fofal_erp TO fofal_user;
```

2. Variables d'environnement (.env)
```env
DATABASE_URL=postgresql://fofal_user:votre_mot_de_passe@localhost/fofal_erp
```

## Redis

### Installation
```bash
sudo apt install redis-server
```

### Configuration
```env
REDIS_URL=redis://localhost:6379
```

## Migrations

1. Initialisation
```bash
alembic init migrations
```

2. Création d'une migration
```bash
alembic revision --autogenerate -m "description"
```

3. Application des migrations
```bash
alembic upgrade head
```
