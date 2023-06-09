# Minerva

Training system solution.

## Project organization

This project is split in multiple projects/repositories.

### Main project

This repository contains as submodules all the related projects.
It contains also the infrastructure needed for this project to run.

### Design Guidelines

### Relational Modal (RM)

### API Specification

### Server Application

### Web Application

## Usage

## Docker

Create an .env file

```properties
NODE_ENV=development
API_PORT=3000
DB_SERVER=localhost
DB_ROOT_PASSWORD=localhost
DB_DATABASE=minerva
DB_USERNAME=minerva
DB_PASSWORD=minerva
DB_PORT=3306
JWT_SECRET=d7a481461577ba4c3c4c6946cca7204b
JWT_EXPIRE=1d
JWT_ISSUER=minerva
JWT_AUDIENCE=web-minerva
```

Start all the services with the provided configuration

```shell
docker compose --env-file .env up 
```

## Portainer

## Development

You can run any service needed for the server application or web application.

- **mysql** MySQL instance
- **web**  Admin web application
- **api** API server application

Start the specified service with the provided configuration

```shell
docker compose --env-file .env up service_name
```
