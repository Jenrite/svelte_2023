<script>
  import Header from "$lib/Header.svelte";
  import Footer from "$lib/Footer.svelte";

  import { onMount } from "svelte";

  const CARD_URL = "https://api.magicthegathering.io/v1/cards?";
  // https://api.magicthegathering.io/v1/cards?subtypes=Vampire&pageSize=1&contains=imageUrl&random=true

  let isLoaded = false;
  let cards = [];

  async function RandomCard() {
    isLoaded = false;
    const res = await fetch(
      `${CARD_URL}subtypes=Vampire&pageSize=2&contains=imageUrl&random=true`
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
  <link rel="stylesheet" href="css/main.css" />
</svelte:head>

<Header />

<div class="button-container">
  <button on:click={() => RandomCard()}>Draw cards</button>
  {#if isLoaded === false}
    <div class="loader" />
  {/if}
</div>

<div class="container">
  <div class="grid">
      {#each cards as card}
        <div class="box">
          <img class="card" src={card.imageUrl} alt="card image" />
        </div>
      {/each}
  </div>
</div>
<Footer />

<style>
  .button-container {
    display: inline-flex;
    align-items: center;
  }

  .loader {
    display: block;
    margin-left: 10px;
    width: 20px;
    height: 20px;
    border: 3px solid white;
    border-radius: 50%;
    animation: spin 7s ease-in-out;
    animation-iteration-count: infinite;
    transition-duration: 0.1s;
  }

  @keyframes spin {
    0% {
      transform: rotate(0deg);
      border-bottom: solid 3px transparent;
      border-top: solid 3px transparent;
    }
    50% {
      transform: rotate(1800deg);
      border: 3px solid white;
      border-left: solid 3px transparent;
      border-right: solid 3px transparent;
    }
    100% {
      transform: rotate(0deg);
      border-bottom: solid 3px transparent;
      border-top: solid 3px transparent;
    }
  }

  .container {
    display: flex;
    justify-content: center;
  }

  .grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
  }

  .card {
    padding: 0%;
    margin: 0%;
  }
  
  .box {
    align-items: center;
    justify-content: center;
    display: inline-flex;
  }

  .card:hover {
    transform: scale(1.2);
    transition: all 0.3s ease 0s;
  }

  button {
    padding: 9px 25px;
    background-color: rgba(229, 75, 75, 1);
    border: none;
    border-radius: 10px;
    cursor: pointer;
    transition: all 0.3s ease 0s;
    margin-left: 10px;
  }

  button:hover {
    background-color: rgba(229, 75, 75, 0.8);
  }
</style>
