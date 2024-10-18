<script>
	import '../app.css';
	import Header from '$lib/components/Header.svelte';
</script>

<div class="app">
	<Header />

	<main>
		<slot />
	</main>

	<footer>
		<p>&copy; 2024 Benjamin Ruhlig. All rights reserved.</p>
	</footer>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
	}

	footer {
		background-color: #343a40;
		color: #fff;
		padding: 1rem;
		text-align: center;
	}
</style>