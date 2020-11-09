<script>
  import Hero from '../components/Hero.svelte'
  import Projects from '../components/Projects.svelte'
  import About from '../components/About.svelte'
  import Contactbar from '../components/Contactbar.svelte'
  import { GoogleAnalytics } from '@beyonk/svelte-google-analytics'
</script>



<svelte:head>
  <title>Eric Amrhein - Web Developer</title>
</svelte:head>

<div>
  <Contactbar />
  <Hero />
  <About />
  <Projects />
</div>
