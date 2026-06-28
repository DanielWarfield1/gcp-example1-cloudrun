# GCP Cloud Run — Vue Example

A Vue 3 SPA deployed to Cloud Run with zero configuration files beyond the app itself.

## Deployment (one-time setup)

1. Go to **Cloud Run → Create Service**
2. Choose **"Continuously deploy from a repository"** and connect this GitHub repo
3. Set the build type to **Google Cloud Buildpacks** (auto-detects Node.js)
4. Set container port to **8080**
5. Click **Create**

Every push to the configured branch triggers a new build and deploy automatically.

Cloud Run runs `npm run build` then `npm start`, which builds the Vite app and serves `dist/` on port 8080.

## Local development

```bash
npm install
npm run dev    # http://localhost:5173
npm start      # serve the production build on http://localhost:8080
```
