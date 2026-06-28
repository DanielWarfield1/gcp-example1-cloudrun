<script setup lang="ts">
const envName = import.meta.env.VITE_ENV_NAME ?? 'local'
const revision = import.meta.env.VITE_REVISION ?? 'dev'
</script>

<template>
  <div class="home">
    <div class="hero">
      <div class="badge">GCP Cloud Run</div>
      <h1>Vue on Cloud Run</h1>
      <p class="subtitle">
        A stateless Vue 3 single-page application served from a containerized Nginx on Google Cloud Run.
      </p>
    </div>

    <section class="cards">
      <div class="card">
        <h2>Stateless by Design</h2>
        <p>
          Cloud Run scales to zero and spins up new instances on demand. This app keeps no server-side
          session state — every request is independent.
        </p>
      </div>
      <div class="card">
        <h2>Container-Native</h2>
        <p>
          Built with Vite, compiled to static assets, and served by Nginx in a minimal Docker image.
          Cloud Run pulls the image from Artifact Registry.
        </p>
      </div>
      <div class="card">
        <h2>Zero Config CI/CD</h2>
        <p>
          Connect this repo in the Cloud Run console and every push automatically builds and deploys.
          No pipeline files needed.
        </p>
      </div>
    </section>

    <div class="meta">
      <span>Environment: <strong>{{ envName }}</strong></span>
      <span>Revision: <strong>{{ revision }}</strong></span>
    </div>
  </div>
</template>

<style scoped>
.home {
  max-width: 900px;
  margin: 0 auto;
  padding: 2rem 1.5rem;
}

.hero {
  text-align: center;
  padding: 3rem 0 2rem;
}

.badge {
  display: inline-block;
  background: #e8f0fe;
  color: #1a73e8;
  font-size: 0.8rem;
  font-weight: 600;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  padding: 0.3rem 0.8rem;
  border-radius: 99px;
  margin-bottom: 1rem;
}

h1 {
  font-size: 2.5rem;
  font-weight: 700;
  color: #202124;
  margin: 0.5rem 0;
}

.subtitle {
  color: #5f6368;
  font-size: 1.1rem;
  max-width: 560px;
  margin: 0.75rem auto 0;
  line-height: 1.6;
}

.cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 1.25rem;
  margin: 2.5rem 0;
}

.card {
  background: #fff;
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  padding: 1.5rem;
}

.card h2 {
  font-size: 1.05rem;
  font-weight: 600;
  margin: 0 0 0.6rem;
  color: #202124;
}

.card p {
  font-size: 0.92rem;
  color: #5f6368;
  line-height: 1.6;
  margin: 0;
}

.meta {
  display: flex;
  gap: 2rem;
  justify-content: center;
  font-size: 0.85rem;
  color: #80868b;
  padding: 1rem 0;
  border-top: 1px solid #e0e0e0;
}
</style>
