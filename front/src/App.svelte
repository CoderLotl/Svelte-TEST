<script>
  import frogLogo from './assets/frog.gif'  
  import Counter from './lib/Counter.svelte'
</script>

<main>
  <div>
    <a href="https://svelte.dev" target="_blank" rel="noreferrer">
      <img src={frogLogo} class="logo frog" alt="Svelte Logo" />
    </a>
  </div>
  <h1>Vite + Svelte</h1>

  <div class="card">
    <Counter />
  </div>
</main>

<style>
  .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
    transition: filter 300ms;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.frog:hover
  {
    filter: drop-shadow(0 0 20px #2caa05);
  }
</style>
