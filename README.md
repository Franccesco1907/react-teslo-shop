# React Teslo Shop

React/Vite storefront with product browsing, JWT login and an admin product editor. API requests use TanStack Query and Axios; auth state uses Zustand.

## Local development

Use Node.js 22.12+ and the committed npm lockfile.

```sh
npm ci
cp .env.template .env
npm run dev
```

Start a compatible Teslo backend separately. `VITE_API_URL` includes the API prefix (default `http://localhost:3000/api`). Open the Vite URL under `/react-teslo-shop/`.

## Checks and layout

`npm run build` type-checks and builds; `npm run lint` runs ESLint. `npm run preview` serves the build. No test script is configured.

`src/app.router.tsx` defines routes; `src/shop`, `src/auth` and `src/admin` own their screens. `src/api/tesloApi.ts` adds the stored bearer token. GitHub Pages deployment runs on pushes to `main`; configure its `VITE_API_URL` repository variable before building.
