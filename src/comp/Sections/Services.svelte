<script>
  import BiCard from "../BiCard.svelte";

  let cards = [
    {
      name: "ГИРОСКУТЕРОВ",
      desc: "ля ля ля",
      filename: "segway_small.png"
    },
    {
      name: "ГИРОСКУТЕРОВ",
      desc: "ля ля ля",
      filename: "segway_small.png"
    }
  ];
</script>

<style>

</style>

<section id="services">
  MDM-SERVICE ЭТО КАЧЕСТВЕННЫЙ РЕМОНТ
  {#each cards as card}
    <BiCard {...card} />
  {/each}

  <!-- КОМПЬЮТЕРОВ И НОУТБУКОВ
МОНОКОЛЕС
ТЕЛЕФОНОВ И ПЛАНШЕТОВ
КВАДРОКОПТЕРОВ
ФОТОАППАРАТОВ И ВИДЕОКАМЕР
РОБОТ - ПЫЛЕСОСОВ
СМАРТ ЧАСОВ
ЭЛЕКТРО ВЕЛОСИПЕДОВ
SEGWAY И АНАЛОГОВ -->
</section>
