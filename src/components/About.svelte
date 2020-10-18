<script>
</script>

<style>
  #about {
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
    padding-left: 15%;
    padding-right: 15%;
  }
  p {
    font-size: 18rem;
    font-weight: normal;
    margin-bottom: 20rem;
  }
  ul {
    display: grid;
    grid-template-columns: repeat(2, minmax(140px, 200px));
    padding: 0px;
    margin: 20px 0px 0px;
  }
  li {
    list-style-type: "▹";
    content: "▹";
    color: cornflowerblue;
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
  #preamble {
    margin-right: 25rem;
  }
  img {
    max-width: 380px;
    height: auto;
    border-radius: 8px;
  }
  @media (max-width: 800px) {
    #inner {
      flex-direction: column;
    }
    #content {
      padding: 5%;
    }
    #inner {
      padding: 0%;
    }
    img {
      max-width: 100%;
    }
    ul {
      margin-bottom: 20rem;
      padding-left: 25%;
      padding-right: 25%;
    }
  }
</style>

<section id="about">
  <div id="content">
    <div id="section-title">
      <h3><span>01. </span>About Me</h3>
      <div id="pad" />
      <div id="divider" />
    </div>
    <div id="inner">
      <div id="preamble">
        <p>Hello!, I'm Eric, a software engineer based in San Francsico, CA.</p>
        <p>
          I enjoyed building things the live on the web, such as websites,
          applications or APIs. My goal is to build performat and minimal
          projects.
        </p>
        <p>
          Apart from building user-friendly and modern applications, I love
          using my knowledge in Web Architecture and Data Structures and
          Algorithms to create scalable applications and to debug complex and
          important problems.
        </p>
        <p>Here are a few Technologies I enjoy working with:</p>
        <ul>
          <li>JavaScript</li>
          <li>React</li>
          <li>HTML & CSSS</li>
          <li>Node.js</li>
          <li>Svelte</li>
        </ul>
      </div>
      <div><img alt="cute-puppy" src="/images/eric.jpg" /></div>
    </div>
  </div>
  <a href="#projects">
    <div id="scrolldown">
      <svg class="arrows">
        <path class="a1" d="M0 0 L30 32 L60 0" />
        <path class="a2" d="M0 20 L30 52 L60 20" />
        <path class="a3" d="M0 40 L30 72 L60 40" />
      </svg>
    </div>
  </a>
</section>
