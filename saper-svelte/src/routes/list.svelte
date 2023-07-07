<script>
    const names = ['Bruce', 'Clark', 'Diana']
    const fullNames = [
        {first: 'Bruce', last:"Wayne"},
        {first: 'Clark', last:"Wayne"},
        {first: 'Princess', last:"Wayne"},
    ]
</script>

<style>
    .text-center{
        text-align: center;
    }
    h2{
        padding: 5px 0;
        font-weight: bold;
    }
</style>

<main class="text-center">
{#each fullNames as name, index}
<h2>{index +1} {name.first} {name.last}</h2>
{/each}

    {#each names as name, index}
    <h3>{index + 1} {name}</h3>
    {/each}
</main>