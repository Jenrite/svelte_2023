<svelte:head>
  <link rel="stylesheet" href="css/main.css" />
</svelte:head>

<script>
  import Header from "$lib/Header.svelte";
  import Footer from "$lib/Footer.svelte";

  import { onMount } from 'svelte'

  const CARD_URL = "https://api.magicthegathering.io/v1/cards?subtypes=Vampire&pageSize=6&contains=imageUrl";

  let cards = [];
    
    onMount(async () => {
        const res = await fetch(`${CARD_URL}`);
        const json = await res.json();
        cards = json.cards;
        console.log(cards);
    })

</script>
<style>

    .grid{
        display:grid;  
        column-gap: 50px;
    }
  

    .card{
        display: inline-flex;  
    }

    .card:hover{
      transform: scale(2);
    }
</style>


<Header />
<div class="grid">
  {#each cards as card}
  <div class ="box">
   <img class="card" src ={card.imageUrl} alt="card image"/> 
</div>
  {/each}
</div>
<Footer />