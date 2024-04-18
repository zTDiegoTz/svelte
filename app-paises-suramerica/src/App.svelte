<script>
  import Countries from "./lib/countries.svelte";
  const list = ["colombia", "venezuela", "ecuador", "peru", "brasil", "bolivia", "argentina"];
</script>

<div class="main">
  {#each list as country}
    <div>
      <Countries {country} />
    </div>
  {:else}
    No existen elementos
  {/each}
</div>

<svelte:head>
  <title>Paises de suramerica</title>
</svelte:head>

<style>
  .main {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-gap: 10px;
    grid-auto-rows: minmax(100px, auto);
  }
</style>
