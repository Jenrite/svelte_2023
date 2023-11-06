<svelte:head>
  <link rel="stylesheet" href="css/main.css" />
</svelte:head>

<script>
  import Header from "$lib/Header.svelte";
  import Footer from "$lib/Footer.svelte";
</script>

<Header />
<div class="container">
    <iframe style="pointer-events: none" width="100%" height="100%" src="https://www.youtube.com/embed/HSsqzzuGTPo?si=-EnZssOUlHeq9U5D&mute=1&autoplay=1" title="YouTube video player" frameborder="0" 
 allowfullscreen></iframe>
    <div class="overlayText">
      <p id="topText">RAHHHHHHHHHHHHHHHHHHHHHHHH
      </p>
    </div>
  </div>

  <style>
  .overlayText {
    position: absolute;
    top: 30%;
    left: 20%;
    z-index: 1;
  }
  
  #topText {
    color: white;
    font-size: 20px;
    align-self: center;
  }
</style>
<Footer />