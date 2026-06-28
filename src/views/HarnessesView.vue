<template>
  <div class="harnesses">
    <h1>Agent Harnesses</h1>
    <p class="sub">A standardized way to give AI agents roles, context, and capabilities.</p>

    <p class="body">
      As agents become more capable, the context they need grows with them — tools,
      memory, role definitions, and domain knowledge all have to land in the right
      place at the right time. Agent Harnesses solve this with a portable directory
      format that enables progressive disclosure: agents load only what's needed for
      each task, keeping things fast without sacrificing depth.
    </p>

    <p class="body">
      Think of a harness as a job title and its constituent skills as individual job
      requirements. The spec defines how to structure that relationship so any
      AI client can discover and use it consistently.
    </p>

    <a href="https://agentharnesses.io" target="_blank" rel="noopener" class="cta">
      Explore the spec at agentharnesses.io →
    </a>
  </div>
</template>

<style scoped>
.harnesses {
  max-width: 640px;
  margin: 0 auto;
  padding: 4rem 1.5rem;
}

h1 {
  font-size: 2.8rem;
  font-weight: 700;
  color: #202124;
  margin: 0 0 0.4rem;
}

.sub {
  font-size: 1.1rem;
  color: #5f6368;
  margin: 0 0 2rem;
}

.body {
  font-size: 1rem;
  color: #3c4043;
  line-height: 1.7;
  margin: 0 0 1.1rem;
}

.cta {
  display: inline-block;
  margin-top: 0.75rem;
  font-size: 0.95rem;
  font-weight: 600;
  color: #1a73e8;
  text-decoration: none;
}

.cta:hover {
  text-decoration: underline;
}
</style>
