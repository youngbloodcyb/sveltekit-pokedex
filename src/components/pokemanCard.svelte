<script>
    export let pokeman;
</script>

<a class="font-press-start p-6 text-center rounded-md hover:shadow-md flex flex-col items-center" href={`/pokemon/${pokeman.id}`}>
    <img class="h-40 w-40" src={pokeman.image} alt={pokeman.name}>
</a>