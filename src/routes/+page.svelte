
<svelte:head>
  <link rel="stylesheet" href="css/main.css" />
</svelte:head>

<script>
  import Header from "$lib/Header.svelte";
  import Footer from "$lib/Footer.svelte";
</script>

<Header />
<div class="container">
    <iframe class="video" style="pointer-events: none" src="https://www.youtube.com/embed/hWagaTjEa3Y?si=KypiLS1GE9xNA-2j&mute=1&autoplay=1" 
    title="YouTube video player" frameborder="0" 
 allowfullscreen></iframe>
    <div class="overlayText">
      <p id="topText">Blehehehhhh
      </p>
    </div>
  </div>

  <style>
.container{
  overflow:hidden;
}

@import url('https://fonts.googleapis.com/css2?family=Inter+Tight&display=swap');

.video {
  /* override other styles to make responsive */
  width: 100vw    !important;
  aspect-ratio: 16 / 9;
  /*height: 100vh   !important;*/
}
  .overlayText {
    position: absolute;
    top: 42%;
    left: 10%;
    z-index: 1;
  }
  
  #topText {
    font-family: 'Inter Tight', sans-serif;
    color: rgba(255, 0, 0, 0.527);
    font-size: 700%;
    align-self: center;
  }
</style>
<Footer />

