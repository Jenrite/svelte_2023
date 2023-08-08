<svelte:head>
  <link rel="stylesheet" href="css/main.css" />
</svelte:head>

<script>
  import Header from "$lib/Header.svelte";
  import Footer from "$lib/Footer.svelte";
</script>

<Header />
<div class="gallerys">
  <a target="_blank" href="drac.jpg">
    <img src="img/drac.jpg" alt="Scary dracula ahh" width="180" height="200" class="center">
  </a>
  <div class="descs">Here is count dracula looking mighty scary!</div>
</div>
<div class="gallerys">
  <a target="_blank" href="drac.jpg">
    <img src="img/draculahandsome.jpg" alt="Scary dracula ahh" width="180" height="200" class="center">
  </a>
  <div class="descs">Here is count dracula looking mighty scary!</div>
</div>
<div class="gallerys">
  <a target="_blank" href="drac.jpg">
    <img src="img/draculamoon.jpg" alt="Scary dracula ahh" width="180" height="200" class="center">
  </a>
  <div class="descs" >Here is count dracula looking mighty scary!</div>
</div>
<br><br><br><br><br><br><br><br><br><br><br><br><br>
<Footer />
