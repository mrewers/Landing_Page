<script>
  export let page;
</script>

<style>
  article {
    background-color: white;
    border-radius: 5px;
    padding: 0.5rem;
  }

  div {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  h3 {
    margin: 0.5rem;
  }

  .github {
    align-self: flex-end;
    margin: 0.5rem 0.75rem 0;
  }

  .screenshot {
    border: solid 1px #bdbdbd;
    border-radius: 2.5px;
    max-width: 100%;
    margin: 0.5rem;
  }
</style>

<article>
  <a href={page.url} target="_blank">
    <div>
      <h3>{page.title}</h3>
      <img class="screenshot" src={page.screenshot} alt="" />

      {#if page.github}
        <a class="github" href={page.github} target="_blank">
          <img alt="See on GitHub" src="/assets/github.svg" />
        </a>
      {/if}
    </div>
  </a>
</article>
