<script>
  import Header from '../components/Header.svelte';

  export let segment;
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Mulish:wght@400;600;700&display=swap');

  :global(*) {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Mulish', sans-serif;
    color: #ffffff;
  }

  :global(a) {
    text-decoration: none;
  }

  :global(input, button) {
    outline: none;
  }

  main {
    padding: 0 1rem;
    background-color: #272343;
  }

  @media (min-width: 768px) {
    main {
      padding: 0 1.25rem;
    }
  }

  @media (min-width: 1024px) {
    main {
      padding: 0 2rem;
    }
  }
</style>

<Header {segment} />

<main>
  <slot />
</main>
