<template>
  <div class="about">
    <h1>How it Works</h1>

    <ol class="steps">
      <li>
        <strong>Push</strong> — A git push triggers Cloud Run's built-in continuous deployment.
      </li>
      <li>
        <strong>Build</strong> — Cloud Run detects the <code>Dockerfile</code>, runs the multi-stage
        build: Node/Vite compiles the app, Nginx serves the static output.
      </li>
      <li>
        <strong>Deploy</strong> — The new container image is deployed to a managed HTTPS endpoint.
      </li>
      <li>
        <strong>Scale</strong> — Cloud Run routes traffic across instances and scales to zero when idle.
      </li>
    </ol>

    <h2>Key Files</h2>
    <ul class="files">
      <li><code>Dockerfile</code> — multi-stage build: Node/Vite → Nginx static serve</li>
      <li><code>nginx.conf</code> — routes all paths to <code>index.html</code> for SPA routing</li>
    </ul>
  </div>
</template>

<style scoped>
.about {
  max-width: 720px;
  margin: 0 auto;
  padding: 2rem 1.5rem;
}

h1 {
  font-size: 2rem;
  font-weight: 700;
  color: #202124;
  margin-bottom: 1.5rem;
}

h2 {
  font-size: 1.3rem;
  font-weight: 600;
  color: #202124;
  margin: 2rem 0 1rem;
}

.steps {
  list-style: none;
  counter-reset: step;
  padding: 0;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.steps li {
  counter-increment: step;
  display: flex;
  align-items: flex-start;
  gap: 1rem;
  background: #fff;
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  padding: 1rem 1.25rem;
  font-size: 0.95rem;
  color: #3c4043;
  line-height: 1.5;
}

.steps li::before {
  content: counter(step);
  background: #1a73e8;
  color: white;
  font-size: 0.8rem;
  font-weight: 700;
  width: 1.6rem;
  height: 1.6rem;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
  margin-top: 0.05rem;
}

.files {
  list-style: none;
  padding: 0;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.files li {
  font-size: 0.92rem;
  color: #3c4043;
}

code {
  background: #f1f3f4;
  padding: 0.15em 0.4em;
  border-radius: 3px;
  font-size: 0.88em;
}
</style>
