<script>
  import Banner from '../components/Banner.svelte'
</script>

<style>
  #two{
    z-index: 1;
    background-color: purple;
  }
</style>

<svelte:head>
  <title>Eric Amrhein - Web Developer</title>
</svelte:head>

<div>
  <Banner />
  <div id="two">
    Projects
  </div>
</div>
