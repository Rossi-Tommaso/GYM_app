<script>
  import Social from "../components/social.svelte"; 
</script>
<svelte:head>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link
    href="https://fonts.googleapis.com/css2?family=Faculty+Glyphic&display=swap"
    rel="stylesheet"
  />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link
      href="https://fonts.googleapis.com/css2?family=Anton+SC&family=Faculty+Glyphic&display=swap"
      rel="stylesheet"
  />
</svelte:head>

<header>
  <h1 class="faculty-glyphic-regular">Fit Tracker</h1>
</header>

<main>
  <slot />
</main>

<footer>
  <Social />
</footer>

<style>
  /*structure*/
  :global(body) {
    margin: 0;
    padding: 0;
    --first-color: #f4d6cc;
    --second-color: #0c1618;
    --third-color: #462418;
    --fourth-color: rgba(70, 19, 2, 0.1);
    overflow: hidden;
  }

  :global(*) {
    margin: 0;
    padding: 0;
  }

  /* fonts */
  :global(.faculty-glyphic-regular) {
    font-family: "Faculty Glyphic", sans-serif;
    font-style: normal;
  }

  :global(.faculty-glyphic-regular) {
    font-family: "Faculty Glyphic", sans-serif;
    font-weight: 400;
    font-style: normal;
  }

  :global(.anton-sc-regular) {
    font-family: "Anton SC", sans-serif;
    font-weight: 400;
    font-style: normal;
  }

  header {
    height: 7.5vh;
    background-color: var(--second-color);
    color: var(--first-color);
    display: flex;
    flex-direction: row;
    align-items: center;
    padding-left: 1.5%;
    font-size: 1.5em;
  }

  main {
    height: 87.5vh;
    background-color: var(--first-color);
  }

  footer {
    height: 5vh;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    background-color: #0c1618;
  }
</style>
