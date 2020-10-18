<script>
  export let project;
</script>

<style>
  #grid-item {
    display: grid;
    gap: 10px;
    grid-template-columns: max-content auto auto auto;
    grid-template-rows: 100%;
    align-items: center;
    margin: 10rem;
    padding-right: 10%;
    padding-left: 10%;
  }

  #text {
    grid-column: 2/2;
    display: flex;
    flex-direction: column;
    justify-content: start;
    height: 100%;
  }
  span {
    color: crimson;
    font-family: monospace;
    font-size: 15rem;
  }
  img {
    max-width: 350px;
    height: auto;
    border-radius: 8px;
    margin: 10rem;
  }
  h4 {
    color: cornflowerblue;
    font-size: 30rem;
    margin-bottom: 20rem;
  }
  p {
    font-size: 18rem;
    font-weight: normal;
    margin-bottom: 20rem;
    padding-right: 10rem;
  }
  #image {
    grid-column: 1/1;
    width: 100%;
  }
  #links {
    display: flex;
    align-items: flex-end;
    height: 100%;
    padding-bottom: 5%;
  }
  @media (max-width: 900px) {
    #grid-item {
      display: flex;
      flex-direction: column;
      padding: 5%;
    }
    img {
      max-width: 100%;
    }
    #image {
      display: flex;
      justify-content: center;
    }
    #text {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
    }
  }
</style>

<div id="grid-item">
  <div id="image">
    <a href={project.github}><img alt={project.title} src={project.img} /></a>
  </div>
  <div id="text">
    <a href={project.github}><h4>{project.title}</h4></a>
    <p>{project.description}</p>
    <div>
      <h3>Technologies:</h3>
      {#each project.technologies as tech}<span> {tech} </span>{/each}
    </div>
    <div id="links">
      <a href={project.github}><p>Github</p></a>
      <a href={project.live}><p>Live</p></a>
    </div>
  </div>
</div>
