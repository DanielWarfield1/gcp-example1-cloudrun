# GCP Cloud Run — Vue Example

A Vue 3 SPA deployed to Cloud Run via Docker.

## Deployment (one-time setup)

1. Go to **Cloud Run → Create Service**
2. Choose **"Continuously deploy from a repository"** and connect this GitHub repo
3. Set the build type to **Dockerfile**
4. Set container port to **8080**
5. Click **Create**

Every push to the configured branch triggers a new build and deploy automatically.

## Local development

```bash
npm install
npm run dev    # http://localhost:5173
```

## Local Docker build

```bash
docker build -t gcp-cloudrun-vue .
docker run -p 8080:8080 gcp-cloudrun-vue
# http://localhost:8080
```
