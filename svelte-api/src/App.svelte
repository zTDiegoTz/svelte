<script>
  import Character from "./lib/Character.svelte";


  let personajes = [];
  let pagina = 1;

  async function personajesrick() {
    const response = await fetch(
      "https://rickandmortyapi.com/api/character?page=" + pagina
    );
    const data = await response.json();
    personajes = data.results;
  }

  personajesrick();

  function paginasiguiente() {
    pagina++;
    personajesrick();
  }

  function paginaanterior() {
    pagina--;
    personajesrick();
  }
</script>

<main class="container">
  <h1 class="title">Rick And Morty Svelte</h1>

  <div class="btns">
    <button class="btn"  on:click={paginaanterior} disabled={pagina === 1}>Anterior</button>
    <button class="btn" on:click={paginasiguiente}>Siguiente</button>
  </div>

  <div class="grid">
    {#each personajes as character}
      <Character {character}/>
    {/each}
  </div>
</main>
