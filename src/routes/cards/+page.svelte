<script>
  import Header from "$lib/Header.svelte";
  import Footer from "$lib/Footer.svelte";

  //onMount lets you exectute code when the page is opened, i use it for my inital card pull

  import { onMount } from "svelte";
 
  const CARD_URL = "https://api.magicthegathering.io/v1/cards?subtypes=Vampire&pageSize=9&contains=imageUrl&random=true";
  // this is my url which i use to fetch, and below me are some items i use later to check if the cards are loaded
  //and an array to put the cards in
  let isLoaded = false;
  let cards = [];

  //this function pulls from the api and populates the array aswell as setting cards.loaded to true to stop displaying
  //the loading icon after the pull is complete by checking the arrays length is greater than 0
  async function RandomCard() {
    isLoaded = false;
    const res = await fetch(
      `${CARD_URL}`
    );
    const json = await res.json();
    cards = json.cards;

    if (cards.length > 0) {
      isLoaded = true;
      
    }

    console.log(cards);
  }

  onMount(async () => {
    RandomCard();
  });
</script>

<svelte:head>
  <link rel="stylesheet" href="../css/styles.css" />
</svelte:head>

<div class="container">
  <Header />
  <!-- this class is a used to call the random card function when 
    the button is clicked + show the loading icon -->
  <div class="button-container">
  <button on:click={() => RandomCard()}>Draw cards</button>
  {#if isLoaded === false}
    <div class="loader" />
  {/if}
</div>
<!--This class sets up the grid of cards + populates the card class with info from
the card array  -->
<div class="container-cards">
  <div class="grid">
      {#each cards as card}
        <div class="box">
          <img class="card" src={card.imageUrl} alt="card image" />
        </div>
      {/each}
  </div>
</div>
</div>
<Footer />

<style>
</style>
