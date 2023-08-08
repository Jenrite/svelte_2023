
<svelte:head>
  <link rel="stylesheet" href="css/main.css" />
</svelte:head>

<script>
  import Header from "$lib/Header.svelte";
  import Footer from "$lib/Footer.svelte";
</script>

<Header />

<h1 class="secondDiv">Welcome to dracula.net</h1>
<img src="drac.jpg" alt="Scary dracula ahh">

<Footer />

<style>



  * {
    text-align: center;
    background-color: white;
    color: black;
    font-family: Helvetica;

  }

</style>
