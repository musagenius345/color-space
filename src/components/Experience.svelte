<script>
  const webTech = ['sass', 'bootstrap', 'css3', 'html5', 'javascript', 'vite', 'neovim', 'powershell', 'vitest', 'markdown', 'pnpm', 'postcss', 'astro', 'git']
</script>
<h2>Web Technologies</h2>
  <div>
{#each webTech as tech}
  <img src="/svg/{tech}.svg" width="80" height="60" alt="{tech}">
{/each}
</div>
  <style>
  div{
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    flex: 0 1 1.6rem;
  gap: .86rem;

  }
  </style>
