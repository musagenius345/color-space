<script lang="ts">
  


</script>

  <!-- <h1>Hello {name}</h1> -->



<nav>
  <ul>
    <li><a href="/Home">Home</a></li>
    <li><a href="Projects">Projects</a></li>
    <li><a href="Contact">About Me</a></li>
    <li><a href="Blog">Blog</a></li>
  </ul>

</nav>

  <style>
    nav{
      max-width: 100vw;
      overflow-x: hidden;
      padding-inline: min(2ch, 1rem);
      /* box-shadow: grey; */
      border-block-end: 3px solid grey;
      /* background-color: oklch(80 0.08 1); */
    }
    ul{
      /* max-width: 100dvw; */
      display: flex;
      gap: 1rem;
      padding-block: .1rem;
      padding-inline: 0.5rem;
      justify-content: space-around;
      align-items: center;
      list-style: none;
    }

    a{
      text-decoration: none;
      color: navy;
      text-transform: uppercase;
      font-size: clamp(.89rem, calc(1rem + .5vw), 1.4rem);
    }
  </style>
