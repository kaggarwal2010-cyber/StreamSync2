# StreamSync

## Run locally

```sh
npm ci
npm run dev
```

## Deploy to GitHub Pages

Push to the `main` branch. The workflow at `.github/workflows/pages.yml` builds this Vite app and deploys `streamsync/dist` to GitHub Pages. In the repository settings, set **Pages > Build and deployment > Source** to **GitHub Actions**. The workflow also supports manual runs from the **Actions** tab.

The app is a static frontend. Its `/actions` requests need a separately hosted backend; GitHub Pages does not run server-side APIs. The demo login and in-browser UI can still be used without that backend, but data persistence and server-backed features will not work.
