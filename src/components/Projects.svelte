<style>
  #project-grid {
    background-color: chartreuse;
    display: grid;
    grid-template-columns: 50% 50%;
    grid-template-rows: 50% 50%;
  }
  #grid-item {
    margin: 1em;
    background: purple;
  }
  section {
    text-align: center;
    padding: 3em;
    height: 40em;
  }
  h2 {
    text-align: left;
  }
</style>

<svelte:head>
  <title>About</title>
</svelte:head>
<section id="projects">
  <h2>Projects</h2>
  <div id="project-grid">
    <div id="grid-item">
      <img alt="cute-puppy" src="http://place-puppy.com/400x400 " />
      <div>
        <p>caption</p>
      </div>
    </div>
    <div id="grid-item">
      <img alt="cute-puppy" src="http://place-puppy.com/400x400 " />
      <div>
        <p>caption</p>
      </div>
    </div>
    <div id="grid-item">
      <img alt="cute-puppy" src="http://place-puppy.com/400x400 " />
      <div>
        <p>caption</p>
      </div>
    </div>
    <div id="grid-item">
      <img alt="cute-puppy" src="http://place-puppy.com/400x400 " />
      <div>
        <p>caption</p>
      </div>
    </div>
  </div>
</section>
