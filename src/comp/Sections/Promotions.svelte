<script>
  import PromotionCard from "../PromotionCard.svelte";

  let cards = [
    {
      text: "Всем пенсионерам!",
      value: 5,
      filename: "segway_small.png"
    },
    {
      text: "Каждое воскресенье!",
      value: 10,
      filename: "segway_small.png"
    },
    {
      text: "Система накопительных скидок!",
      value: "3-10",
      filename: "segway_small.png"
    }
  ];
</script>

<style lang="scss">
  section{
    &::before{
      content: "";
      display: block;
      background: red;
      height: 1em;
      width: 100%;
    }
  }
</style>

<section id="promotions">
  <h1>НАШИ АКЦИИ!</h1>
  <div class="grid">
    {#each cards as card}
      <PromotionCard {...card} />
    {/each}
  </div>
</section>
