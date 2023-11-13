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


<div id="container">
  <div class="card">
    <img src="https://upload.wikimedia.org/wikipedia/commons/8/8b/YouTube_dark_icon_%282017%29.svg" alt="Youtube logo"/>
    <div class="card_details">
      <div class="name">My youtube</div>
      <button>Youtube</button>
    </div>
  </div>
</div>



<style>
  @import url("https://fonts.googleapis.com/css2?family=Raleway:wght@500;600&display=swap");

  .grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
  }

  body {
  background-color: #eaeff1;
  font-family: "Raleway", sans-serif;
}

img {
  width: 100%;
  border-radius: 12px;
  height: 214px;
  object-fit: cover;
}

#container {
  max-width: 300px;

  /* Center the container in middle on horizontal axis */
  margin: 0 auto;

  /* Add empty space above the container (20% of the view height) */
  margin-top: 20vh;
}

.card {
  /* Change background color */
  background-color: white;

  /* Add border */
  border: 1px solid #bacdd8;

  /* Add space between the border and the content */
  padding: 8px;

  border-radius: 12px;
}
.card_details {
  /* Add space around the details */
  padding: 16px 8px 8px 8px;
}
button {
  border: none;
  padding: 12px 24px;
  border-radius: 50px;

  font-weight: 600;
  color: #0077ff;
  background-color: #e0efff;

  /* Button is inline-block element by default, it need to have block display for margin: 0 auto; to work */
  margin: 0 auto;
  display: block;

  /* Button is a clickable element, therefore it should have a pointer cursor */
  cursor: pointer;
}
.name {
  font-size: 24px;
  font-weight: 600;

  margin-top: 16px;
}


</style>
