<script>
	import Button from "./Button.svelte";
	let button = {
		icon: "account_circle",
		size: "large",
		label: "User",
	};
</script>

<svelte:head>
	<link
		href="https://fonts.googleapis.com/icon?family=Material+Icons"
		rel="stylesheet"
	/>
</svelte:head>

<main>
	<Button {...button} />
	<Button icon="lock" color="white" backgroundColor="maroon" size="medium" label="Sperren" />
	<Button icon="lock" color="white" backgroundColor="maroon" size="small" />
	<Button color="white" backgroundColor="black" size="medium" label="Help!" />
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
