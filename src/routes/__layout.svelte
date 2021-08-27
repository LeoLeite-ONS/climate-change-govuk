<script>
  import './../styles/reset.css';
  import './../styles/globals.css';

  import Header from '$lib/header/Header.svelte';
  import Navigation from '$lib/Navigation.svelte';
</script>

<!-- https://dev.to/lenaschnedlitz/create-a-simple-dark-mode-toggle-with-svelte-4b3g  -->

<Header />

<div class="container">
  <Navigation />

  <main>
    <slot></slot>
  </main>
</div>
