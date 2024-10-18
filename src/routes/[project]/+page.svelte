<script>
	import { page } from '$app/stores';

	const projects = {
		'project-1': {
			name: 'Project 1',
			description: 'Detailed description of Project 1...',
			link: 'https://project1.example.com'
		},
		'project-2': {
			name: 'Project 2',
			description: 'Detailed description of Project 2...',
			link: 'https://project2.example.com'
		},
		'project-3': {
			name: 'Project 3',
			description: 'Detailed description of Project 3...',
			link: 'https://project3.example.com'
		}
	};

	$: project = projects[$page.params.project];
</script>

<svelte:head>
	<title>{project.name} - Your Name CV</title>
</svelte:head>

<h1>{project.name}</h1>
<p>{project.description}</p>
<a href={project.link} target="_blank" rel="noopener noreferrer">View Project</a>

<style>
	h1 {
		margin-bottom: 1rem;
	}

	p {
		margin-bottom: 1rem;
	}

	a {
		display: inline-block;
		padding: 0.5rem 1rem;
		background-color: #0077b5;
		color: white;
		text-decoration: none;
		border-radius: 4px;
	}

	a:hover {
		background-color: #005fa3;
	}
</style>