<script>
  export let type = "button";
  export let disabled = false;
  export let autofocus = false;
  export let value = "";
  export let name = "";
  export let buttonType = "";
</script>

<style lang="scss">
  button {
    display: block;
    text-decoration: none;
    font-weight: 300;
    margin: 0;
    color: var(--light-color);
    padding: 3px;
    padding-left: 5px;
    padding-right: 5px;
    transition: 0.5s;
    background-color: var(--dark-color);
    border: var(--dark-color) 1px solid;
    padding: 0 20px;
    border-left-color: var(--dark-color-light);
    font-size: var(--font-size);
    font-family: var(--font-family);

    &:hover {
      top: 5px;
      transition: 0.5s;
      background-color: var(--light-color);
      border: var(--light-color) 1px solid;
      color: var(--dark-color);
      cursor: pointer;
    }

    &:focus {
      outline: 0;
    }

    @media (max-width: 440px) {
      font-size: 14px;
    }
    @media (max-width: 380px) {
      font-size: 3vw;
    }

    &.request {
      background-color: var(--main-color);
      border: var(--main-color) 1px solid;
      box-shadow: 0 0 0
        rgba(
          var(--main-color-red),
          var(--main-color-green),
          var(--main-color-blue),
          1
        );
      animation: pulse 2s infinite;

      &:hover {
        background-color: var(--light-color);
        border: var(--light-color) 1px solid;
        animation: none;
      }
    }
  }

  @keyframes pulse {
    0% {
      -moz-box-shadow: 0 0 0 0
        rgba(
          var(--main-color-red),
          var(--main-color-green),
          var(--main-color-blue),
          0.8
        );
      box-shadow: 0 0 0 0
        rgba(
          var(--main-color-red),
          var(--main-color-green),
          var(--main-color-blue),
          0.8
        );
    }
    70% {
      -moz-box-shadow: 0 0 0 20px
        rgba(
          var(--main-color-red),
          var(--main-color-green),
          var(--main-color-blue),
          0
        );
      box-shadow: 0 0 0 20px
        rgba(
          var(--main-color-red),
          var(--main-color-green),
          var(--main-color-blue),
          0
        );
    }
    100% {
      -moz-box-shadow: 0 0 0 0
        rgba(
          var(--main-color-red),
          var(--main-color-green),
          var(--main-color-blue),
          0
        );
      box-shadow: 0 0 0 0
        rgba(
          var(--main-color-red),
          var(--main-color-green),
          var(--main-color-blue),
          0
        );
    }
  }
</style>

<button
  class={buttonType === 'request' ? 'request' : ''}
  {type}
  {name}
  {value}
  {disabled}
  on:click>
  <slot />
</button>
