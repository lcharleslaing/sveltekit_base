<script>
  export let title = "Title Goes Here!";
</script>

<div class="title">
  <div class="title-card">
    <img width="45px" height="45px" src="static\favicon.png" alt="Site Logo" />
    <h1>{title}</h1>
  </div>
</div>

<style>
  .title {
    background-color: #f5f5f5;
    border-bottom: 1px solid #d5d5d5;
    padding: 10px;
    text-align: center;
    display: flex;
    /* center horizontal and vertical */
    align-items: center;
    justify-content: center;
    /* radius */
    border-radius: 0.5rem;
    margin-bottom: 5px;
    /* background image with transparency */
    background-image: url("static/usaflag.jpg");
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
  }
  .title-card {
    /* card */
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    /* radius */
    border-radius: 0.5rem;
    /* background image with transparency */
    background-color: #f5f5f5;
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    padding: 5px;
    height: 50px;
    /* shadow */
    box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.75);
  }
  img {
    margin-right: 10px;
  }
</style>
