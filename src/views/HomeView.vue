<template>
  <div class="home">
    <section class="hero">
      <h1>Daniel Warfield</h1>
      <p class="tagline">AI — intuitively and exhaustively explained.</p>
    </section>

    <section class="projects">
      <a class="card" href="https://iaee.substack.com" target="_blank" rel="noopener">
        <h2>Intuitively and Exhaustively Explained</h2>
        <p>
          The ultimate source in AI, for beginners and experts alike. Deep dives on neural
          networks, transformers, RAG, and the latest in AI research — written to make
          complex ideas genuinely scrutable.
        </p>
        <span class="link">Read on Substack →</span>
      </a>

      <RouterLink class="card" to="/harnesses">
        <h2>Agent Harnesses</h2>
        <p>
          A standardized format for giving AI agents roles, context, and capabilities.
          Structure your agents so they load only what they need — fast, portable, and composable.
        </p>
        <span class="link">Learn more →</span>
      </RouterLink>
    </section>
  </div>
</template>

<style scoped>
.home {
  max-width: 780px;
  margin: 0 auto;
  padding: 4rem 1.5rem;
}

.hero {
  margin-bottom: 3rem;
}

h1 {
  font-size: 2.8rem;
  font-weight: 700;
  color: #202124;
  margin: 0 0 0.4rem;
}

.tagline {
  font-size: 1.15rem;
  color: #5f6368;
  margin: 0;
}

.projects {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1.25rem;
}

.card {
  display: block;
  background: #fff;
  border: 1px solid #e0e0e0;
  border-radius: 10px;
  padding: 1.75rem;
  text-decoration: none;
  transition: border-color 0.2s, box-shadow 0.2s;
}

.card:hover {
  border-color: #1a73e8;
  box-shadow: 0 2px 12px rgba(26, 115, 232, 0.1);
}

.card h2 {
  font-size: 1.1rem;
  font-weight: 600;
  color: #202124;
  margin: 0 0 0.75rem;
}

.card p {
  font-size: 0.92rem;
  color: #5f6368;
  line-height: 1.65;
  margin: 0 0 1.25rem;
}

.link {
  font-size: 0.88rem;
  font-weight: 600;
  color: #1a73e8;
}
</style>
