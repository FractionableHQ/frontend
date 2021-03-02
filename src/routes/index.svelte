<script>
  import { goto } from "@sapper/app";
  import { Menu, Button } from "../components";
</script>

<style lang="scss">
  section {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: flex-start;
  }
</style>


<h1>Fractionable</h1>
<h2 class="space-top">» Where collectibles meet DeFi</h2>

<ul class="large-space-top large-space-bottom">
  <li><span class="bold">Artists.</span> Fractionate NFTs into fungible ERC20s.</li>
  <li><span class="bold">Owners.</span> Own a share of NFTs or gain exposure to community curated NFTs indexes.</li>
  <li><span class="bold">Developers.</span> Use NFTs shares as collateral in any DeFi protocol.</li>
</ul>

<section>
  <Button class="space-right">explore</Button>
  <Button>fractionate</Button>
</section>
