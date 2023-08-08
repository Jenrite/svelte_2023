
<svelte:head>
  <link rel="stylesheet" href="css/main.css" />
</svelte:head>

<script>
  import Header from "$lib/Header.svelte";
  import Footer from "$lib/Footer.svelte";
</script>

<Header />

<h1 class="secondDiv">Welcome to Dracula.net</h1>

<div class="center2">
<iframe width="1280px" height="720px" src="https://www.youtube.com/embed/NcBjx_eyvxc?autoplay=1&mute=1" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen ></iframe>
</div>

<Footer />

<style>



  * {
    text-align: center;
    background-color: white;
    color: black;
    font-family: Helvetica;

  }

</style>
