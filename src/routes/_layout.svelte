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
  #banner {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 35em;
    opacity: 1;
    background: url("/background.png");
    background-repeat: repeat;
    background-position: 50% 50%;
    z-index: -1;
    pointer-events: none;
  }

  :global(button) {
    display: inline-block;
    cursor: pointer;
    padding: 0.5em 2em;
    background: none;
    border: 0.15em solid #ffffff;
    margin: 0 0.3em 0.3em 0;
    border-radius: 0.2em;
    box-sizing: border-box;
    text-decoration: none;
    color: #ffffff;
    text-align: center;
    font-weight: bold;
    transition: all 0.2s;
  }
  :global(button):hover {
    color: #000000;
    background-color: #ffffff;
  }
</style>

<div id="banner" />
<Nav {segment} />
<main>
  <slot />
</main>
