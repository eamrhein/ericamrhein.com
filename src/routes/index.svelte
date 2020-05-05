<script>
  function handleClick() {
    alert("testing");
  }
</script>

<style>
  #img {
    position: absolute;
    background: url("/background.png");
    height: 42em;
    width: 100%;
    z-index: -2;
    pointer-events: none;
    background-size: 500px;
    transform: skew(0deg, -5deg);
    margin-top: -300px;
  }
  #img-mask {
    position: absolute;
    z-index: -1;
    background: rgba(0, 0, 0, 0.6);
    height: 42em;
    pointer-events: none;
  }
  #lead {
    margin-top: 9em;
    text-align: center;
    height: 20em;
  }

  #about {
    display: flex;
    justify-content: space-around;
    height: 20em;
    margin-top: 9em;
  }
  .photo {
    height: 15em;
    width: 15em;
    background: white;
  }
  #photo-wrap {
    margin: 2em;
  }
  #about-text {
    align-self: center;
    margin: 2em;
    max-height: 20em;
  }
  img {
    height: 100%;
    width: 100%;
  }
  h1 {
    color: #e34234;
    font-size: 2.8em;
    font-weight: 700;
    margin: 0 0 0.5em 0;
  }
  h2 {
    color: #679267;
    font-weight: bolder;
  }
  p {
    margin: 1em auto;
  }

  @media (min-width: 480px) {
    h1 {
      font-size: 4em;
    }
  }
  @media (max-width: 480px) {
    #about {
      display: block;
      text-align: center;
    }
    .photo {
      margin-left: auto;
      margin-right: auto;
    }
  }
</style>

<svelte:head>
  <title>Eric Amrhein - Web Developer</title>
</svelte:head>
<div id="img" />
<div id="img-mask" />

<section id="lead">
  <h1>Eric Amrhein</h1>
  <h2>Web Developer</h2>
  <p>San Francisco, California</p>
  <div id="button-row">
    <button on:click={handleClick}>Resume</button>
    <button>Email</button>
    <button>Github</button>
    <button>LinkedIn</button>
  </div>
</section>
<section id="about">
  <div id="photo-wrap">
    <div class="photo">
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
