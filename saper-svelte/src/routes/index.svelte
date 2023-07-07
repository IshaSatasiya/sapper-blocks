<script>
	import successkid from 'images/successkid.jpg';
	let user = { loggedIn: false };
	function toggle() {
		user.loggedIn = !user.loggedIn;
	}
</script>

<style>
	h1, figure, p {
		text-align: center;
		margin: 0 auto;
	}

	h1 {
		font-size: 2.8em;
		text-transform: uppercase;
		font-weight: 700;
		margin: 0 0 0.5em 0;
	}

	figure {
		margin: 0 0 1em 0;
	}

	img {
		width: 100%;
		max-width: 400px;
		margin: 0 0 1em 0;
	}

	p {
		margin: 1em auto;
	}

	.text-center{
		text-align: center;
	}

	button{
		padding: 10px 30px;
		background-color: #444;
		border: 1px solid #444;
		color: #fff;
	}

	@media (min-width: 480px) {
		h1 {
			font-size: 4em;
		}
	}
</style>

<svelte:head>
	<title>Sapper project template</title>
</svelte:head>

<h1>Great success!</h1>

<figure>
	<img alt="Success Kid" src="{successkid}">
	<figcaption>Have fun with Sapper!</figcaption>
</figure>

<div class="text-center">
{#if user.loggedIn}
	<button on:click={toggle}> Log out </button>
	<p>you are logged out</p>
{/if}

{#if !user.loggedIn}
	<button on:click={toggle}> Log in </button>
	<p>you are logged in</p>
{/if}
</div>
