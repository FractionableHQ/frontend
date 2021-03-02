<script>
  import { Header, Main, Nav } from "../components";

  export let segment;
  let opened = false;
</script>

<style lang="scss" global>
  @import 'reset.scss';
  @import 'global.scss';
</style>

<Nav bind:opened {segment} />
<Header bind:opened />
<Main><slot {segment} /></Main>
