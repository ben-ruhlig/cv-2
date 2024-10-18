<script>
	const skills = [
		{ name: 'JavaScript', projects: ['Project 1', 'Project 2'] },
		{ name: 'React', projects: ['Project 1'] },
		{ name: 'Node.js', projects: ['Project 2', 'Project 3'] },
		{ name: 'Python', projects: ['Project 3'] },
	];
</script>

<section id="skills">
	<h2>Technical Expertise</h2>
	<ul class="skills-list">
		{#each skills as skill}
			<li>
				<span class="skill-name">{skill.name}</span>
				<div class="project-tags">
					{#each skill.projects as project}
						<span class="project-tag">{project}</span>
					{/each}
				</div>
			</li>
		{/each}
	</ul>
</section>

<style>
	.skills-list {
		list-style-type: none;
		padding: 0;
		max-width: 800px;
		margin: 0 auto;
	}

	.skills-list li {
		background-color: #fff;
		margin-bottom: 1rem;
		padding: 1rem;
		border-radius: 8px;
		box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
		display: flex;
		justify-content: space-between;
		align-items: center;
		flex-wrap: wrap;
	}

	.skill-name {
		font-weight: bold;
		font-size: 1.2rem;
		color: #343a40;
		margin-right: 1rem;
	}

	.project-tags {
		display: flex;
		gap: 0.5rem;
		flex-wrap: wrap;
	}

	.project-tag {
		background-color: #007bff;
		color: #fff;
		padding: 0.2rem 0.5rem;
		border-radius: 4px;
		font-size: 0.8rem;
	}
</style>