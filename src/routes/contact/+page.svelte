<script>
  import Header from "$lib/Header.svelte";
  import Footer from "$lib/Footer.svelte";

  async function myFunc() {
    //display card name
  }
</script>

<svelte:head>
  <!-- <link rel="stylesheet" href="css/main.css" /> -->
</svelte:head>

<Header />
<!-- <h1 class="textstyle">Contact me here</h1> -->
<!-- <a href="https://github.com/Jenrite" target="_blank">Github</a>
<a href="https://www.youtube.com/channel/UCLoUDPH17yCM_1eG8dbdT7Q" target="_blank">Youtube</a>
<a href="https://www.instagram.com/6mogu/" target="_blank">Instagram</a> -->

<div class="container" on:click={() => myFunc()}>
  <div class="card">
    <img
      src="https://upload.wikimedia.org/wikipedia/commons/b/b8/YouTube_Logo_2017.svg"
      alt="Avatar"
      style="width:50%"
    />
    <h4><b>John Doe</b></h4>
    <p>Architect & Engineer</p>
  </div>
</div>

<Footer />

<style>
  .card {
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    transition: 0.3s;
    border-radius: 5px; /* 5px rounded corners */
    background-color: bisque;
    justify-content: center;
    width: 20%;
    display:flex;
    flex-direction: column;
  }

  /* Add rounded corners to the top left and the top right corner of the image */
  img {
    border-radius: 5px 5px 0 0;
  }

  .container {
    padding: 2px 16px;
  }
</style>
