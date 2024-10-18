<script>
	const projects = [
		{ name: 'Project 1', thumbnail: '/project1-thumb.jpg', slug: 'project-1' },
		{ name: 'Project 2', thumbnail: '/project2-thumb.jpg', slug: 'project-2' },
		{ name: 'Project 3', thumbnail: '/project3-thumb.jpg', slug: 'project-3' },
	];
</script>

<section id="projects">
	<h2>Featured Projects</h2>
	<div class="project-grid">
		{#each projects as project}
			<a href="/{project.slug}" class="project-card">
				<img src={project.thumbnail} alt={project.name} />
				<h3>{project.name}</h3>
			</a>
		{/each}
	</div>
</section>

<style>
	.project-grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
		gap: 2rem;
		max-width: 1200px;
		margin: 0 auto;
	}

	.project-card {
		border: 1px solid #dee2e6;
		border-radius: 8px;
		overflow: hidden;
		text-decoration: none;
		color: inherit;
		transition: transform 0.3s ease, box-shadow 0.3s ease;
		background-color: #fff;
	}

	.project-card:hover {
		transform: translateY(-5px);
		box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
	}

	.project-card img {
		width: 100%;
		height: 200px;
		object-fit: cover;
	}

	.project-card h3 {
		padding: 1rem;
		margin: 0;
		font-size: 1.2rem;
		color: #343a40;
		text-align: center;
	}
</style>