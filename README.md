# deploy

## Exigences
  - docker
  - docker-compose

## Installation
```bash
git clone https://github.com/PP-Groupe-6/deploy/
cd deploy/
docker-compose up
```
## Structure
  - docker-compose.yml : démarre tous les conteneurs 
  - account : dockerfile pour le conteneur account-microservice
  - transfer : dockerfile pour le conteneur transfer-microservice
  - invoice : dockerfile pour le conteneur invoice-microservice
  - sql : fichiers .sql pour créer et ajouter des éléments à la base de données postgresql
 (- nginx : load balancer et reverse-proxy mais non fonctionnel)
 
 
