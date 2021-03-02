<script>
  let _class
  export { _class as class };
</script>

<style lang="scss">
  button/*, input[type="submit"], input[type="reset"]*/ {
    // reset
    background: none;
    color: inherit;
    border: none;
    padding: 0;
    cursor: pointer;
    outline: inherit;

    // style
    background: $foreground;
    color: $background;
    padding: $GU;

    &:hover {
      background: $accent;
    }
  }
</style>

<button class={_class}>
  <slot />
</button>