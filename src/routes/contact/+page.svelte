<script>
  import Header from "$lib/Header.svelte";
  import Footer from "$lib/Footer.svelte";  

  // i felt like my page needed a little more javascript so i set up this array 
  //with the info i display in my boxes
  let boxes = [
    { id: 1, name: 'Youtube', imageSrc: 'https://cdn1.iconfinder.com/data/icons/social-media-circle-7/512/Circled_Youtube_svg-1024.png', link: 'https://www.youtube.com/channel/UCLoUDPH17yCM_1eG8dbdT7Q' },
    { id: 2, name: 'Instagram', imageSrc: 'https://cdn1.iconfinder.com/data/icons/social-media-circle-7/512/Circled_Instagram_svg-1024.png', link: 'https://www.instagram.com/6mogu/' },
    { id: 3, name: 'Github', imageSrc: 'https://upload.wikimedia.org/wikipedia/commons/c/c2/GitHub_Invertocat_Logo.svg', link: 'https://github.com/Jenrite' }
  ];

  function handleButtonClick(link) {
    window.location.href = link;
  }
</script>

<svelte:head>
   <link rel="stylesheet" href="../css/styles.css" />  
</svelte:head>


<div class="container">
  <Header />
  <main>
<!-- This foreach loop simply applies the info from my array to the boxes, and runs the function for the links to work -->
    {#each boxes as box (box.id)}
      <div class="linkbox" key={box.id}>
        <img class="linkimage" src={box.imageSrc} alt={box.name} />
        <h3>{box.name}</h3>
        <button class="" on:click={() => handleButtonClick(box.link)}>Visit Profile</button>
      </div>
    {/each}
  </main>
  <Footer />

</div>




<style> 
/* here are the styles for my contact page, mainly centering and aligning the boxes
+ scaling the images correctly */
main {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
  }

  .linkbox {
    text-align: center;
    border-radius: 10px;
    padding: 20px;
    margin: 10px;
    background: #2d333a;
  }

  .linkimage {
    max-width: 10vh;
    border-radius: 50%;
  }

</style>
