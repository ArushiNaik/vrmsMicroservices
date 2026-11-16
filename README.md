# Vehicle Registration Microservices 🚗

**Java · Spring Boot · REST APIs · PostgreSQL · Docker Compose · Gradle**

Coordinate vehicle registration across cars, owners and agents. Independent Spring services sit behind an API gateway, with separate database containers for the domain services.

[Portfolio](https://github.com/ArushiNaik) · [Browse source](https://github.com/ArushiNaik/vrmsMicroservices)

## What to explore

- Service boundaries organized around business domains.
- Gateway routing to downstream services.
- Domain validation, API DTOs and persistence adapters.
- Cross-service workflow orchestration.
- Controller, service and domain test sources.

## A guide to the code

- `api-gateway` — routing and API documentation
- `cars-service` — domain API, business logic, persistence and tests
- `owners-service` — domain API, business logic, persistence and tests
- `agents-service` — domain API, business logic, persistence and tests
- `registration-service` — domain API, business logic, persistence and tests
- `docker-compose.yml` — service and database containers

## Run locally

Install Docker Desktop and start the Compose stack from the root:

```bash
docker compose up --build
```

Review `docker-compose.yml` for exposed ports and local settings. Gateway configuration under `api-gateway/src/main/resources` defines routes and API documentation paths.

For individual service development, open its Gradle project and use the Java toolchain declared in its `build.gradle`. Each service has its own configuration and database needs. For example:

```bash
cd cars-service
./gradlew test
```

Windows: `gradlew.bat test`. Do not assume one root Gradle task covers all services.

## Project notes

Tests and container startup were not rerun for this documentation refresh. Test profiles and infrastructure requirements vary by service; inspect the corresponding configuration before running a suite.

## Context

A project in [Arushi Naik’s portfolio](https://github.com/ArushiNaik).
