<script>
	import Introduction from '$lib/components/Introduction.svelte';
	import Projects from '$lib/components/Projects.svelte';
	import Skills from '$lib/components/Skills.svelte';
	import Experiences from '$lib/components/Experiences.svelte';
</script>

<svelte:head>
	<title>Your Name - CV</title>
	<meta name="description" content="Professional CV of Your Name" />
</svelte:head>

<Introduction />
<Projects />
<Skills />
<Experiences />

<style>
	:global(section) {
		padding: 4rem 2rem;
	}

	:global(section:nth-child(odd)) {
		background-color: #f8f9fa;
	}

	:global(section:nth-child(even)) {
		background-color: #e9ecef;
	}

	:global(h2) {
		font-size: 2.5rem;
		text-align: center;
		margin-bottom: 2rem;
		color: #343a40;
		text-transform: uppercase;
		letter-spacing: 2px;
	}

	:global(h2::after) {
		content: '';
		display: block;
		width: 50px;
		height: 3px;
		background-color: #007bff;
		margin: 1rem auto 0;
	}
</style>