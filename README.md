# Chappy

## Module Ownership and Boundaries

- `src/backend/`: Backend service code, API surfaces, and server-side domain logic.
- `src/frontend/`: Frontend application workspace and all client-side UI/state modules.
  - `src/frontend/src/components/`: Shared UI components.
  - `src/frontend/src/pages/`: Route-level page modules.
  - `src/frontend/src/lib/`: Reusable frontend utilities and client adapters.
  - `src/frontend/src/hooks/`: Reusable frontend hooks.
  - `src/frontend/src/stores/`: Frontend state containers/stores.
  - `src/frontend/src/types/`: Frontend-specific type declarations.
- `shared/`: Cross-cutting contracts/utilities intended for both frontend and backend usage.
- `docs/`: Architecture notes, RFCs, and operational documentation.

### Boundary Rules

1. Backend-only concerns stay in `src/backend/` and do not import frontend modules.
2. Frontend-only concerns stay in `src/frontend/` and do not import backend modules.
3. Shared code in `shared/` must remain framework-agnostic and safe for both runtimes.
4. Documentation and design decisions are recorded in `docs/`.
