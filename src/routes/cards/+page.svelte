<script>
  import Header from "$lib/Header.svelte";
  import Footer from "$lib/Footer.svelte";

  import { onMount } from "svelte";

  const CARD_URL = "https://api.magicthegathering.io/v1/cards?";
  // https://api.magicthegathering.io/v1/cards?subtypes=Vampire&pageSize=1&contains=imageUrl&random=true

  let cards = [];

  async function RandomCard() {
    const res = await fetch(
      `${CARD_URL}subtypes=Vampire&pageSize=9&contains=imageUrl&random=true`
    );
    const json = await res.json();
    cards = json.cards;
  }

  onMount( async () => {
    RandomCard();
  })
</script>

<svelte:head>
  <link rel="stylesheet" href="css/main.css" />
</svelte:head>

<Header />
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
    display: inline-flex;
    padding: 0%;
    margin: 0%;
  }

  .card:hover {
    transform: scale(1.2);
    transition: all 0.3s ease 0s;
  }
</style>
