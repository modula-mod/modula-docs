<script lang="ts">
  export let title = 'Docs';
</script>

<div class="modula-docs-page">
  <header class="docs-header">
    <h1>{title}</h1>
    <p>Documentation and guides for Modula.</p>
  </header>

  <section class="docs-grid">
    <article class="docs-card">
      <h2>Getting Started</h2>
      <p>Learn the basics of Modula, modules, plugins, and surfaces.</p>
    </article>

    <article class="docs-card">
      <h2>Modules</h2>
      <p>Understand how modules expose widgets, pages, profile tabs, and capabilities.</p>
    </article>

    <article class="docs-card">
      <h2>Plugins</h2>
      <p>See how plugins extend parent modules through extension slots and capabilities.</p>
    </article>

    <article class="docs-card">
      <h2>Board</h2>
      <p>Explore how Board widgets are added, rendered, and persisted.</p>
    </article>

    <article class="docs-card">
      <h2>Marketplace</h2>
      <p>Browse, install, update, and diagnose packages through the Marketplace.</p>
    </article>

    <article class="docs-card">
      <h2>Developer CLI</h2>
      <p>Use the Modula CLI to create, validate, build, preview, and publish packages.</p>
    </article>
  </section>

  <section class="docs-meta">
    <p><strong>Route:</strong> /docs</p>
    <p><strong>Package:</strong> docs</p>
    <p><strong>Namespace:</strong> modula.docs</p>
  </section>
</div>

<style>
  .modula-docs-page {
    display: grid;
    gap: 1.25rem;
  }

  .docs-header p {
    margin-top: 0.5rem;
    color: rgba(15, 23, 42, 0.72);
  }

  .docs-grid {
    display: grid;
    gap: 1rem;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  }

  .docs-card {
    border: 1px solid rgba(15, 23, 42, 0.08);
    border-radius: 1rem;
    padding: 1rem;
    background: rgba(255,255,255,0.72);
  }

  .docs-meta {
    opacity: 0.8;
    font-size: 0.95rem;
  }

  :global(html.dark) .docs-card,
  :global(html.oled-dark) .docs-card {
    border-color: rgba(255,255,255,0.08);
    background: rgba(15, 23, 42, 0.35);
  }

  :global(html.dark) .docs-header p,
  :global(html.oled-dark) .docs-header p {
    color: rgba(226, 232, 240, 0.78);
  }
</style>
