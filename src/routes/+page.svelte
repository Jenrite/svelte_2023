<!-- This is my script tag, its in all my pages and simply imports the header and footer so they can be used in the site  -->
<script>
  import Header from "$lib/Header.svelte";
  import Footer from "$lib/Footer.svelte";
</script>

<!-- this is my stylesheet link which pulls from my styles.css file -->
<svelte:head>
  <link rel="stylesheet" href="../css/styles.css" /> 
</svelte:head>


<div class="container">
  <Header />
  <!-- my iframe is set up so the user cannot interact with it or the ui, acting like a background -->
    <iframe
      class="video"
      style="pointer-events: none"
      src="https://www.youtube.com/embed/hWagaTjEa3Y?si=KypiLS1GE9xNA-2j&mute=1&autoplay=1"
      title="YouTube video player"
      frameborder="0"
      allowfullscreen
    />
<!-- This is my typed logo for my page, i'll get into how its done in styles.css -->
    <div class="wrapper">
      <div class="typing-demo">
        Welcome to vampire.net
      </div>
  </div>
  <div class="hpText"><h1>Enjoy your stay</h1></div>
</div>

<Footer />
