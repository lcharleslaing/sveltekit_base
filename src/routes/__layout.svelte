<script>
  import Title from "$lib/components/Title.svelte";
  import Navbar from "$lib/components/Navbar.svelte";
  import "$lib/styles/global.css";
</script>

<div class="main">
  <header>
    <Title title="Title goes here!" />
  </header>

  <Navbar />

  <main>
    <!-- page content -->
    <slot />
  </main>

  <footer>
    <p class="footer-text">Copyright 2022 Big2Tiny</p>
  </footer>
</div>

<style>
  .main {
    margin: 10px;
  }
  footer {
    background-color: white;
    color: black;
    padding: 0.1rem;
    text-align: center;
    font-weight: bold;
    /* radius */
    border-radius: 0.5rem;
  }
  header {
    /* radius */
    border-radius: 0.5rem;

    /* box shadow */
    box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.75);
  }
  footer {
    background-color: #f5f5f5;
    padding: 0.1rem;
    /* box shadow */
    box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.75);
    /* background image with transparency */
    background-image: url("static/usaflag.jpg");
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    height: 50px;
    /* lock to bottom of screen */
    position: fixed;
    bottom: 10px;
    width: 95%;
  }
  .footer-text {
    display: flex;
    background-color: #f5f5f5;
    font-size: 0.8rem;
    /* card that is the same width as text */
    width: fit-content;
    /* center the text */
    margin: auto;
    border-radius: 0.5rem;
    /* box shadow */
    box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.75);
    padding: 5px;
    /* center vertically */
    align-self: center;
    margin-top: 12px;
  }
</style>
