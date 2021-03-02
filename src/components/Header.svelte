<script>
  import { stores } from "@sapper/app";
  import { Burger } from "./index.js";
  export let opened
</script>

<style lang="scss">
  header {
    display: flex;
    flex-direction: row;
    align-items: flex-end;
    justify-content: stretch;
    height: 4 * $GU;
    padding: 0 $space;

    img {
      height: 3 * $GU;
    }

    input {
      flex: 1 1 auto;
      border-bottom: 1px solid $accent;
      color: $accent;
      font-size: 2 * $GU;
      line-height: 3 * $GU;
      height: 3 * $GU;

      @include placeholder() {
        color: transparentize($accent, 0.8);
      }
    }
  }
</style>

<header>
  <img src="/img/logo.png" alt="Fractionable" class="large-space-right">
  <input type="text" placeholder="search fractionable" class="large-space-right"/>
  <Burger bind:opened />
</header>
