<script>
	import { onMount } from 'svelte';

	const experiences = [
		{ 
			title: 'Senior Developer',
			company: 'Tech Corp',
			date: '2020 - Present',
			description: 'Led development of multiple high-impact projects...'
		},
		{
			title: 'Web Developer',
			company: 'StartUp Inc',
			date: '2018 - 2020',
			description: 'Developed and maintained various web applications...'
		},
		{
			title: 'Junior Developer',
			company: 'Code Solutions',
			date: '2016 - 2018',
			description: 'Assisted in the development of client websites...'
		}
	];

	let selectedExperience = null;

	function openModal(experience) {
		selectedExperience = experience;
	}

	function closeModal() {
		selectedExperience = null;
	}

	onMount(() => {
		document.addEventListener('keydown', (e) => {
			if (e.key === 'Escape') closeModal();
		});
	});
</script>

<section id="experiences">
	<h2>Professional Journey</h2>
	<div class="timeline">
		{#each experiences as experience}
			<div class="timeline-item" on:click={() => openModal(experience)}>
				<div class="timeline-content">
					<h3>{experience.title}</h3>
					<p class="company">{experience.company}</p>
					<p class="date">{experience.date}</p>
				</div>
			</div>
		{/each}
	</div>
</section>

{#if selectedExperience}
	<div class="modal-backdrop" on:click={closeModal}>
		<div class="modal" on:click|stopPropagation>
			<h3>{selectedExperience.title}</h3>
			<h4>{selectedExperience.company}</h4>
			<p class="date">{selectedExperience.date}</p>
			<p>{selectedExperience.description}</p>
			<button on:click={closeModal}>Close</button>
		</div>
	</div>
{/if}

<style>
	.timeline {
		position: relative;
		max-width: 800px;
		margin: 0 auto;
	}

	.timeline::after {
		content: '';
		position: absolute;
		width: 4px;
		background-color: #007bff;
		top: 0;
		bottom: 0;
		left: 50%;
		margin-left: -2px;
	}

	.timeline-item {
		padding: 10px 40px;
		position: relative;
		background-color: inherit;
		width: 50%;
		cursor: pointer;
	}

	.timeline-item::after {
		content: '';
		position: absolute;
		width: 20px;
		height: 20px;
		right: -10px;
		background-color: #fff;
		border: 4px solid #007bff;
		top: 15px;
		border-radius: 50%;
		z-index: 1;
	}

	.timeline-item:nth-child(odd) {
		left: 0;
	}

	.timeline-item:nth-child(even) {
		left: 50%;
	}

	.timeline-item:nth-child(even)::after {
		left: -10px;
	}

	.timeline-content {
		padding: 20px;
		background-color: #fff;
		position: relative;
		border-radius: 6px;
		box-shadow: 0 2px 5px rgba(0,0,0,0.1);
	}

	.timeline-content h3 {
		margin: 0;
		color: #343a40;
	}

	.timeline-content .company {
		color: #6c757d;
		font-style: italic;
	}

	.timeline-content .date {
		color: #007bff;
		font-weight: bold;
	}

	.modal-backdrop {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-color: rgba(0, 0, 0, 0.5);
		display: flex;
		justify-content: center;
		align-items: center;
		z-index: 1000;
	}

	.modal {
		background-color: white;
		padding: 2rem;
		border-radius: 8px;
		max-width: 500px;
		width: 90%;
	}

	button {
		margin-top: 1rem;
		padding: 0.5rem 1rem;
		background-color: #007bff;
		color: white;
		border: none;
		border-radius: 4px;
		cursor: pointer;
		transition: background-color 0.3s ease;
	}

	button:hover {
		background-color: #0056b3;
	}
</style>