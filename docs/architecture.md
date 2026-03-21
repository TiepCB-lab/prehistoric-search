# Architecture

## Overview
Prehistoric Search follows a layered backend architecture and a feature-oriented frontend architecture. The backend exposes a REST API, and the frontend consumes it as a React SPA.

## Backend Layers
- Controller: receives HTTP requests and delegates to services.
- Request: validates and normalizes incoming API payloads.
- DTO: transfers validated data into the application layer.
- Service: coordinates use cases and business rules.
- Repository: abstracts persistence and query details.
- Model: represents Eloquent entities and relationships.
- Provider: registers bindings and bootstrapping concerns.

## Frontend Layers
- Pages: route-level screens.
- Features: domain-specific UI and state modules.
- Components: reusable presentation building blocks.
- Services: API communication layer.
- Hooks: reusable client-side behavior.
- Types and Utils: shared contracts and helper utilities.

## Data Flow
1. The user interacts with the React SPA.
2. A page or feature module calls a frontend service.
3. The service sends a request to the Laravel API.
4. A request class validates input.
5. A controller forwards the request to a service.
6. The service uses repositories to query or persist data.
7. Repositories interact with Eloquent models and PostgreSQL.
8. The API returns structured data to the SPA for rendering.

## Scalability Notes
- Search concerns are isolated in dedicated services and DTOs.
- Reference data is separated from creature records to support future domains.
- The architecture is creature-agnostic, allowing mammals, marine reptiles, and other prehistoric life to be added later.
