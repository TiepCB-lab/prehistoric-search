# Prehistoric Search

Prehistoric Search is a scalable full-stack web application skeleton for exploring prehistoric creatures through feature-based search. The initial domain focuses on dinosaurs, while the architecture remains generic enough to support other prehistoric life in future iterations.

## Tech Stack
- Backend: Laravel, PostgreSQL, REST API
- Frontend: React, TypeScript, Vite SPA
- Architecture: Controller -> Service -> Repository -> Model

## Folder Structure
```text
prehistoric-search/
├─ backend/
│  ├─ app/
│  ├─ bootstrap/
│  ├─ config/
│  ├─ database/
│  └─ routes/
├─ frontend/
│  └─ src/
├─ docs/
├─ README.md
└─ .gitignore
```

## Backend Setup
1. `cd backend`
2. `composer install`
3. Copy `.env.example` to `.env`
4. Configure PostgreSQL credentials in `.env`
5. Run `php artisan key:generate`
6. Run `php artisan migrate --seed`
7. Start the API with `php artisan serve`

## Frontend Setup
1. `cd frontend`
2. `npm install`
3. Copy `.env.example` to `.env`
4. Set `VITE_API_BASE_URL=http://127.0.0.1:8000/api/v1`
5. Start the SPA with `npm run dev`

## Development Roadmap
- Establish the Laravel and React foundations
- Build the core creature catalog and relationships
- Implement search filters and query optimization
- Connect the SPA to the REST API
- Add autocomplete, recommendations, and performance improvements

## Notes
- This repository currently contains an architecture-first skeleton only.
- Business logic, schema details, and production dependencies should be added during implementation.
