<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css" integrity="sha512-SnH5WK+bZxgPHs44uWIX+LLJAJ9/2PkPKZ5QiAj6Ta86w+fsb2TkcmfRyVX3pBnMFcV7oQPJkl9QevSCWr3W6A==" crossorigin="anonymous" referrerpolicy="no-referrer" />
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

<main>
  <header></header>
  <h1 class="title">Rick and morty </h1>
  <hr>

  <div class="container">
   
   
   

    <div class="grid">
      {#each personajes as character}
        <Character {character}/>
      {/each}
    </div>

    <div class="btns">
      <button class="btn"  on:click={paginaanterior} disabled={pagina === 1}>
         <i class="fa-solid fa-chevron-left"></i>
         Anterior
      </button>

      <button class="btn" on:click={paginasiguiente}>
        Siguiente
        <i class="fa-solid fa-chevron-right"></i>
        
      </button>
      
    </div>

  </div>
  <footer>@Luis Cuelllo</footer>
  
</main>
