<style lang="scss">
  main {
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
    max-width: 1500px;
    width: fit-content;
    padding: $GU;
    margin: auto;
    min-height: calc(100vh -  10 * #{$GU} - 2 * #{$GU});
  }
</style>

<main><slot /></main>