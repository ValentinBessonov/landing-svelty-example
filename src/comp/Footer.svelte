<script>
  import Button from "./Button.svelte";
</script>

<style>
  footer {
    background-color: var(--dark-color);
    width: 100%;
    height: 64px;
    display: -webkit-flex;
    display: flex;
    -webkit-flex-direction: row;
    flex-direction: row;
    justify-content: center;
  }
</style>

<footer>
  <Button>ПРОВЕРИТЬ СТАТУС ВАШЕГО РЕМОНТА</Button>
  <Button buttonType="request">ОСТАВИТЬ ЗАЯВКУ НА ДИАГНОСТИКУ</Button>
</footer>
