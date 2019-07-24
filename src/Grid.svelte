<script>
  import GridItem from "./GridItem.svelte";
  import { pages } from "./pages.js";
</script>

<style>
  article {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-gap: 1rem;
  }

  @media screen and (max-width: 1000px) {
    article {
      grid-template-columns: 1fr 1fr;
    }
  }

  @media screen and (max-width: 500px) {
    article {
      grid-template-columns: 1fr;
    }
  }
</style>

<article>
  {#each pages as page}
    <GridItem {page} />
  {/each}
</article>
