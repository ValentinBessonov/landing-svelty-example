<script>
  import MdmLogo from "../Logo/MdmLogo.svelte";
  import P5 from "../Logo/P5.svelte";
  import P310 from "../Logo/P310.svelte";
  import P10 from "../Logo/P10.svelte";

  let cards = [
    {
      text: "Всем пенсионерам!",
      value: 5,
      svg: P5
    },
    {
      text: "Каждое воскресенье!",
      value: 10,
      svg: "segway_small.png"
    },
    {
      text: "Система накопительных скидок!",
      value: "3-10",
      svg: "segway_small.png"
    }
  ];
</script>

<style lang="scss">
  section {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background: var(--dark-color);
    color: var(--light-font-color);
  }

  .row {
    display: flex;
    flex-direction: row;
    justify-content: center;
  }

  .grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-gap: 2vw;
    margin: 1em;
  }

  @media (max-width: 750px) {
    .grid {
      grid-template-columns: 1fr;
      grid-template-rows: 1fr 1fr 1fr;
      grid-gap: 4vw;
    }
  }

  .card {
    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    overflow: hidden;
    font-size: 2em;
    border: 1px solid var(--light-color);
    background: var(--dark-color-light);
    padding: 1em;
    p {
      margin: 0 1em 1em 1em;
    }
  }
</style>

<header>
  <link
    href="https://fonts.googleapis.com/css?family=Nunito&display=swap"
    rel="stylesheet" />
</header>

<section id="promotions">
  <MdmLogo />
  <div class="row">
    <h1>ДАРИТ АКЦИИ!</h1>
  </div>
  <div class="grid">
    <div class="card">
      <p>{cards[2].text}</p>
      <P310 />
    </div>
    <div class="card">
      <p>{cards[0].text}</p>
      <P5 />
    </div>
    <div class="card">
      <p>{cards[1].text}</p>
      <P10 />
    </div>
  </div>
</section>
