# Minerva

Training management system solution.

## Key features

- Integrate A.I. to help trough tasks.

## Project organization

This project is split in multiple projects/repositories.

### Main project

This repository contains all the related projects.
It also contains the infrastructure needed for this project to run.

### Design Guidelines & Assets

Logos, typography and color palettes guidelines.

[minerva-design-guidelines](https://github.com/alexandrelamberty/minerva-design-guidelines)

### Entity relationship Model (RM)

Business Analysis of the basic requirement of the system.

[minerva-erm](https://github.com/alexandrelamberty/minerva-erm)

### Relational Modal (RM)

Database structure of the system.

[minerva-rm](https://github.com/alexandrelamberty/minerva-rm)

### API Specification

OpenAPI specification describing how to interact with the system.

[minerva-api-spec](https://github.com/alexandrelamberty/minerva-erm)

### Server Application

Server application exposing an API that implement the above specification.

[minerva-api](https://github.com/alexandrelamberty/minerva-api)

### Web Application

Web application that consume the above API to interact with the system.

[minerva-web-app](https://github.com/alexandrelamberty/minerva-web-app)

### Website

Business website that provide a catalog of trainings that you can enroll on.

[minerva-website](https://github.com/alexandrelamberty/minerva-website)

## Requirements

- [Docker](https://docs.docker.com/get-started/overview/)
- [Docker Compose](https://docs.docker.com/compose/)

## Usage

### Docker

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
OPENAI_API_KEY=d7a481461577ba4c3c4c6946cca7204b
VITE_API_URL=http://localhost:3000
```

Start all the services with the provided configuration

```shell
docker compose --env-file .env up 
```

### Portainer

## Development

You can run any service needed for the server application or web application.

- **mysql** MySQL instance
- **web**  Admin web application
- **api** API server application

Start the specified service with the provided configuration

```shell
docker compose --env-file .env up service_name
```
