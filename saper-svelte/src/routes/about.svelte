<svelte:head>
	<title>About</title>
</svelte:head>

<script>
let count = 0

function handClick(){
	count +=1
}

function newClick(event, stepSize) {
	count += stepSize
}
</script>

<main>
<button on:click={() => (count = count +1)}>Count {count}</button>
<button on:click={handClick}>Count {count}</button>
<button on:click={(event) => newClick(event, 5)}>Count {count}</button>
<button on:click={(event) => newClick(event, 10)}>Count {count}</button>
</main>