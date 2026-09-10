# filmkritiken-frontend

[![Build](https://github.com/DerBlum/filmkritiken-frontend/actions/workflows/build_push.yml/badge.svg)](https://github.com/DerBlum/filmkritiken-frontend/actions/workflows/build_push.yml)

Vue 3 + Vite + Tailwind Cinema-Glass Frontend for the Filmkritiken App.

## Development Server

Run `npm install`, then create a `.env` from `.env.example` (`VITE_API_URL=http://localhost:8080`).

Run `npm run dev` for a dev server. Navigate to `http://localhost:5173/`.

You also need a backend on port 8080. On a managed Windows machine without admin rights,
where the endpoint protection blocks freshly built binaries, see
`docs/local-dev-windows-av.md` in the `filmkritiken-backend` checkout — it describes a
Node stub API to develop the frontend against.

## Build

Run `npm run build` to build the production application. Output is generated in `dist/`.

## Unit Tests

Run `npm run test:unit` to execute Vitest unit tests.
 
