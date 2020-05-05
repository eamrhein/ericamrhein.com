<script>
  import Nav from "../components/Nav.svelte";

  export let segment;
</script>

<style>
  main {
    position: relative;
    margin: 0 auto;
    box-sizing: border-box;
  }
  :global(body) {
    color: #fff;
    background-color: #010101;
  }
</style>

<Nav {segment} />

<main>
  <slot />
</main>
