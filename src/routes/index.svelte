<script>
  import Projects from "../components/Projects.svelte";
  function handleClick() {
    alert("testing");
  }
</script>

<style>
  #lead {
    text-align: center;
    margin-top: 7em;
    margin-bottom: 7em;
  }

  #about {
    padding: 2em;
    background-color: #101010;
    display: flex;
    justify-content: space-evenly;
  }
  .headshot {
    height: 15em;
    width: 15em;
  }
  #photo-wrap {
    margin: 2em;
  }
  #about-text {
    align-self: center;
    margin: 2em;
    max-height: 20em;
  }
  .headshot img {
    height: 100%;
    width: 100%;
    -moz-border-radius: 10px;
    -webkit-border-radius: 10px;
    border-radius: 10px; /* future proofing */
    -khtml-border-radius: 10px; /* for old Konqueror browsers */
  }
  h1 {
    color: #e34234;
  }
  @media (max-width: 480px) {
    #lead {
      margin-bottom: 2em;
    }
    #about {
      display: block;
      text-align: center;
    }
    .headshot {
      margin-left: auto;
      margin-right: auto;
    }
  }
</style>

<svelte:head>
  <title>Eric Amrhein - Web Developer</title>
</svelte:head>
<section id="lead">
  <h1>Eric Amrhein</h1>
  <h5>
    a software developer passionate about building software and learning new
    technologies
  </h5>
  <p>Based in San Francisco, California</p>
  <div id="button-row">
    <button on:click={handleClick}>Resume</button>
    <button>Email</button>
    <button>Github</button>
    <button>LinkedIn</button>
  </div>
</section>
<section id="about">
  <div id="photo-wrap">
    <div class="headshot">
      <img alt="Headshot" src="eric.jpg" />
    </div>
  </div>
  <div id="about-text">
    <h2>About Me</h2>
    <p>
      I am a full-stack software engineer experienced in
      <strong>
        JavaScript, React.js, Redux, Ruby on Rails, Node.js, Express.js, and
        SQL.
      </strong>
      Apart from building user-friendly and modern applications, I love using my
      knowledge in Web Architecture and Data Structures and Algorithms to create
      scalable applications and to debug complex and important problems.
    </p>
  </div>
</section>
<Projects />
