<script>
  import Home from "./Home.svelte";
  import Promotions from "./Promotions.svelte";
  import Services from "./Services.svelte";
  import About from "./About.svelte";
  import Contacts from "./Contacts.svelte";
</script>

<style lang="scss">
  .main {
    height: 100%;
    width: 100vw;
    position: relative;
    padding-bottom: 0;
    box-sizing: border-box;
    overflow: auto;
    scroll-behavior: smooth;
    perspective: 1px; 
    transform-style: preserve-3d;
    overflow-y: scroll;
    overflow-x: hidden;

     &::before {
      content: "";
      display: block;
      position: absolute;
      width: 100vw;
      left: 0;
      right: 0;
      bottom: 0;
      top: 0;
      z-index: -1;
      transform-origin: center;
      min-height: 100vh;
      background-image: url("static/img/main.jpg");
      background-repeat: no-repeat;
      background-size: cover;
      /* Параллакс */
      transform: translateZ(-1px) scale(2);
      filter: opacity(0.4);
    }
  }
</style>

<div class="main">
  <Home />
  <Promotions />
  <Services />
  <About />
  <Contacts />
</div>
