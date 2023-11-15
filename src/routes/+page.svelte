<script>
  import Header from "$lib/Header.svelte";
  import Footer from "$lib/Footer.svelte";
</script>

<svelte:head>
  <link rel="stylesheet" href="css/main.css" />
</svelte:head>

<div class="container">
  <Header />
  <iframe
    class="video"
    style="pointer-events: none"
    src="https://www.youtube.com/embed/hWagaTjEa3Y?si=KypiLS1GE9xNA-2j&mute=1&autoplay=1"
    title="YouTube video player"
    frameborder="0"
    allowfullscreen
  />
  <div class="wrapper">
    <div class="typing-demo">
      Welcome to vampire.net
    </div>
</div>
  
</div>

<Footer />
<style>
  .container {
    overflow: hidden;
  }

  @import url("https://fonts.googleapis.com/css2?family=Inter+Tight&display=swap");

  .video {
    /* override other styles to make responsive */
    width: 100% !important;
    aspect-ratio: 16 / 9;
    /*height: 100vh   !important;*/
  }

  .wrapper {
  /*This part is important for centering*/
  z-index: 1;
  position: absolute;
  left: 12%;
  top: 42%;
}

.typing-demo {
  width: 22ch;
  animation: typing 2s steps(22), blink .5s step-end infinite alternate;
  white-space: nowrap;
  overflow: hidden;
  border-right: 3px solid;
  font-family: monospace;
  font-size: 900%;
  background: -webkit-linear-gradient(#b11c1c, #333);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

@keyframes typing {
  from {
    width: 0
  }
}
    
@keyframes blink {
  50% {
    border-color: transparent
  }
}
</style>
