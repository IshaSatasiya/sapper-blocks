<script>
const num = 1
</script>

<main class="text-center">
    {#if num === 0}
    <h2>The number is zero</h2>
    {:else if num < 0}
    <h2>The number is negative</h2>
    {:else if num > 0}
    <h2>The number is positive</h2>
    {:else}
    <h2>Not a number</h2>
    {/if}
</main>

<style>
    .text-center{
        text-align: center;
    }
    h2{
        padding-top: 5px;
        font-weight: bold;
    }
</style>