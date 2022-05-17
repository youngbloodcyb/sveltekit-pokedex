<script>
    import {pokemon} from "../stores/pokeStore.js";
    import PokemanCard from "../components/pokemanCard.svelte";
    
    let searchTerm = '';
    let filteredPokemon = [];

    $: {
        if (searchTerm) {
            filteredPokemon = $pokemon.filter(pokeman => pokeman.name.toLowerCase().includes(searchTerm.toLowerCase()));
        } else {
            filteredPokemon = [...$pokemon];
        }
    }
</script>

<svelte:head>
    <title>Cam's Pokedex</title>
</svelte:head>

<h1 class="font-press-start text-4xl text-center my-8 uppercase">
    Sveltekit Pokedex
</h1>

<input type="text" placeholder="Search Pokemon" class="font-press-start w-full rounded-md text-lg p-4 border-2 border-gray-200" bind:value={searchTerm} />

<div class="py-4 grid md:grid-cols-3 grid-cols-1">
    {#each filteredPokemon as pokeman}
        <PokemanCard pokeman={pokeman}/>
    {/each}
</div>