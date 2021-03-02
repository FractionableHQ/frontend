<script>
  export let opened = false;
</script>

<style lang="scss">
  div.burger {
    @include transparent();
    cursor: pointer;
    position: relative;
    z-index: 3;
    height: 3 * $GU;
    width: 3 * $GU;
    transition: all 1s $ease;

    span {
      background-color: $accent;
      display: block;
      margin: 2px auto;
      position: absolute;
      left: 0.5 * $GU;
      right: 0.5 * $GU;
      height: $GU / 8;
      width: 2 * $GU;
      transition: all 1s $ease, top 0.3s ease 0.1s;

      &:nth-of-type(1) {
        top: $GU / 2;
        transition: background-color 1s $ease, top 0.3s $ease 0.3s,
          transform 0.3s ease-out 0.1s;
      }
      &:nth-of-type(2) {
        width: 0.5 * $GU;
        top: 1.25 * $GU;
        right: 0.5 * $GU;
        transition: background-color 1s $ease, opacity 0.3s $ease 0.3s;
      }
      &:nth-of-type(3) {
        top: 2 * $GU;
        transition: background-color 1s $ease, top 0.3s $ease 0.3s,
          transform 0.3s ease-out 0.1s;
      }
    }

    &:hover {
      span {
        background-color: $foreground;
      }
    }

    &.opened {
      background-color: $foreground;

      span {
        background-color: $background;

        &:nth-of-type(1) {
          top: 1.5 * $GU;
          transform: rotate(45deg);
          transition: top 0.3s ease 0.1s, transform 0.3s ease-out 0.5s;
        }
        &:nth-of-type(2) {
          opacity: 0;
          transition: top 0.3s ease 0.1s;
        }
        &:nth-of-type(3) {
          top: 1.5 * $GU;
          transform: rotate(-45deg);
          transition: top 0.3s ease 0.1s, transform 0.3s ease-out 0.5s;
        }
      }
    }
  }
</style>

<div
  class="burger {opened ? 'opened' : ''}"
  on:click={() => {
    opened = !opened;
  }}>
  <span />
  <span />
  <span />
</div>
