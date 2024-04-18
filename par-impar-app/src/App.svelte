<script>
  import ParImpar from "./lib/ParImpar.svelte";
  let valor = 0;
  const listenInput = (event) => (valor = event.target.value);
</script>

<main>
  <ParImpar number={valor} />
  <input value on:input={listenInput} />
</main>

<style>
</style>
