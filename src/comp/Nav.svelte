<script>
  $: hash = window.location.hash;
  $: description = "Главная";

  window.onhashchange = function(e) {
    hash = window.location.hash;

    switch (hash) {
      case "#main":
        description = "Главная";
        break;
      case "#promotions":
        description = "Акции";
        break;
      case "#services":
        description = "Услуги";
        break;
      case "#about":
        description = "О нас";
        break;
      case "#contacts":
        description = "Контакты";
        break;

      default:
        break;
    }
  };
</script>

<style lang="scss">
  nav {
    width: 100%;
    display: -webkit-flex;
    display: flex;
    -webkit-flex-direction: row;
    flex-direction: row;
    justify-content: center;
    border-bottom: 1px solid rgba(255, 62, 0, 0.1);
    font-weight: 300;
  }

  ul {
    margin: 0;
    padding: 0;

    &::after {
      content: "";
      display: block;
      clear: both;
    }
  }

  li {
    display: block;
    float: left;
  }

  .selected {
    position: relative;
    display: inline-block;
    color: var(--main-color);

    &::after {
      position: absolute;
      content: "";
      width: calc(100% - 1em);
      height: 2px;
      background-color: var(--main-color);
      display: block;
      bottom: -1px;
    }
  }

  a {
    text-decoration: none;
    font-weight: bold;
    padding: 1em 0.5em;
    display: block;
    color: var(--dark-color);
    text-transform: uppercase;
    transition: 0.5s;

    &:hover {
      transition: 0.5s;
      color: var(--main-color);
    }
    @media (max-width: 440px) {
      font-size: 14px;
    }
    @media (max-width: 380px) {
      font-size: 3vw;
    }
  }
</style>

<svelte:head>
  <title>MDM-SERVICE: {description}</title>
</svelte:head>

<nav>
  <ul>
    <li>
      <a class={hash === '#main' ? 'selected' : ''} href="#main">Главная</a>
    </li>
    <li>
      <a class={hash === '#promotions' ? 'selected' : ''} href="#promotions">
        Акции
      </a>
    </li>
    <li>
      <a class={hash === '#services' ? 'selected' : ''} href="#services">
        Услуги
      </a>
    </li>
    <li>
      <a class={hash === '#about' ? 'selected' : ''} href="#about">О нас</a>
    </li>
    <li>
      <a class={hash === '#contacts' ? 'selected' : ''} href="#contacts">
        Контакты
      </a>
    </li>
  </ul>
</nav>
