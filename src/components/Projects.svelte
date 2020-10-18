<script>
  import Project from './project.svelte'
  import projectData from './projects.js'
</script>

<style>
  #projects {
    /* height: calc(var(--vh, 1vh) * 100); */
    background-color: #101010;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
  }
  #content {
    padding-top: 60rem;
    padding-left: 10%;
    padding-right: 10%; 
  }
  h3 {
    flex-grow: 0;
    font-size: 38rem;
  }
  #section-title {
    display: flex;
    flex-direction: row;
    align-items: center;
  }
  #pad {
    padding: 3rem;
  }
  @media (max-width: 800px) {
    #inner {
      flex-direction: column;
    }
    #content {
      padding: 5%;
    }
  }
  #divider {
    flex-grow: 1;
    height: 1px;
    background-color: #9f9f9f;
  }
  #inner {
    display: flex;
    justify-content: center;
    margin: 1%;
    padding: 1%;
    width: 100%;
  }

  .arrows {
    justify-content: center;
    align-items: center;
    cursor: pointer;
    width: 60px;
    height: 72px;
  }
  #scrolldown {
    display: flex;
    justify-content: center;
  }
  .arrows path {
    stroke: #2994d1;
    fill: transparent;
    stroke-width: 1.5px;
    animation: arrow 2s infinite;
    -webkit-animation: arrow 2s infinite;
  }

  @keyframes arrow {
    0% {
      opacity: 0;
    }
    40% {
      opacity: 1;
    }
    80% {
      opacity: 0;
    }
    100% {
      opacity: 0;
    }
  }

  @-webkit-keyframes arrow /*Safari and Chrome*/ {
    0% {
      opacity: 0;
    }
    40% {
      opacity: 1;
    }
    80% {
      opacity: 0;
    }
    100% {
      opacity: 0;
    }
  }

  .arrows path.a1 {
    animation-delay: -1s;
    -webkit-animation-delay: -1s; /* Safari 和 Chrome */
  }

  .arrows path.a2 {
    animation-delay: -0.5s;
    -webkit-animation-delay: -0.5s; /* Safari 和 Chrome */
  }

  .arrows path.a3 {
    animation-delay: 0s;
    -webkit-animation-delay: 0s; /* Safari 和 Chrome */
  }
  span {
    color: cornflowerblue;
  }

</style>

<section id="projects">
  <div id="content">
    <div id="section-title">
      <h3><span>02. </span>Projects</h3>
      <div id="pad" />
      <div id="divider" />
    </div>
    <div id="inner">
      <div>
        {#each projectData as pObj}
          <Project project={pObj}  />
        {/each}
      </div>
    </div>
</section>