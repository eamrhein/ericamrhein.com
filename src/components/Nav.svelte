<script>
  import { onDestroy } from "svelte";
  export let segment;
  let hash = "";
  const checkhash = () => {
    if (window.location.hash) {
      hash = window.location.hash;
    } else {
      hash = "";
    }
  };
  console.log(hash);
</script>

<style>
  nav {
    border-bottom: 1px solid rgba(227, 66, 52, 0.1);
    font-weight: 500;
    padding: 0 0.5em;
    color: white;
    position: fixed;
    top: 0;
    left: 0;
  }

  ul {
    margin: 0;
    padding: 0;
  }

  /* clearfix */
  ul::after {
    content: "";
    display: block;
    clear: both;
  }

  li {
    display: block;
    float: left;
  }

  [aria-current] {
    position: relative;
    display: inline-block;
  }

  [aria-current]::after {
    position: absolute;
    content: "";
    width: calc(100% - 1em);
    height: 2px;
    background-color: #e34234;
    display: block;
    bottom: -1px;
  }

  a {
    text-decoration: none;
    padding: 0.5em 0.5em;
    display: block;
  }
</style>

<svelte:window on:popstate={checkhash} />
<nav>
  <ul>
    <li>
      <a
        aria-current={segment === undefined && hash === '' ? 'page' : undefined}
        href="">
        about
      </a>
    </li>
    <li>
      <a
        aria-current={hash === '#projects' ? 'page' : undefined}
        href="#projects">
        projects
      </a>
    </li>

    <!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
    <li>
      <a
        rel="prefetch"
        aria-current={segment === 'blog' ? 'page' : undefined}
        href="blog">
        blog
      </a>
    </li>
  </ul>
</nav>
