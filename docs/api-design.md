# API Design

## Versioning
- Base path: `/api/v1`

## Creature Endpoints
- `GET /creatures`: List creatures with pagination and optional sorting.
- `POST /creatures`: Create a creature record.
- `GET /creatures/{id}`: Retrieve a single creature by identifier.
- `PUT /creatures/{id}`: Replace a creature record.
- `PATCH /creatures/{id}`: Partially update a creature record.
- `DELETE /creatures/{id}`: Remove a creature record.

## Search Endpoints
- `GET /search`: Search creatures by keyword and filters.
- `GET /search/autocomplete`: Return search suggestions for future enhancement.

## Reference Data Endpoints
- `GET /reference/taxa`: Return taxonomy filter options.
- `GET /reference/periods`: Return geological period filter options.
- `GET /reference/habitats`: Return habitat filter options.
- `GET /reference/features`: Return feature filter options.

## Response Design Notes
- Use consistent JSON envelopes for success, errors, and pagination metadata.
- Keep filtering parameters explicit and URL-friendly.
- Reserve room for future sorting, faceting, and recommendation fields.
