<script>
  import {onMount} from 'svelte';

  let count = 0;
  onMount(() => {
    const interval = setInterval(() => count++, 1000);
    return () => {
      clearInterval(interval);
    };
  });
</script>

<div class="text-center">
  <header class="text-2xl bg-white text-gray-600 flex flex-col items-center justify-center min-h-screen">
    <img src="/logo.svg" class="h-96 pointer-events-none mb-12 animate-pulse" alt="logo" />
    <p>Edit <code>src/App.svelte</code> and save to reload.</p>
    <p>Page has been open for <code>{count}</code> seconds.</p>
    <p>
      <a class="text-red-500" href="https://svelte.dev" target="_blank" rel="noopener noreferrer">
        Learn Svelte
      </a>
    </p>
  </header>
</div>

<style>
  @tailwind base;
  @tailwind components;
  @tailwind utilities;
  
  :global(body) {
    @apply m-0 font-sans;
  }

  code {
    @apply bg-gray-900 px-2 py-1 rounded;
  }
  
  p {
    @apply m-1.5;
  }
</style>
