<script>
	import { base } from '$app/paths';
</script>

<section id="introduction">
	<h2>Welcome</h2>
	<img src="{base}/your-image.jpg" alt="Your Name" />
	<h1>Your Name</h1>
	<p>Short introduction about yourself goes here. Highlight your key strengths and career objectives.</p>
	<div class="contact-info">
		<a href="mailto:your.email@example.com">your.email@example.com</a>
		<a href="https://twitter.com/your-profile" target="_blank" rel="noopener noreferrer">X Profile</a>
		<a href="https://www.linkedin.com/in/your-profile" target="_blank" rel="noopener noreferrer">LinkedIn</a>
	</div>
</section>

<style>
	section {
		text-align: center;
	}

	h1 {
		font-size: 2.5rem;
		margin: 1rem 0;
		color: #343a40;
	}

	img {
		width: 200px;
		height: 200px;
		border-radius: 50%;
		object-fit: cover;
		border: 4px solid #007bff;
	}

	p {
		max-width: 600px;
		margin: 1rem auto;
		line-height: 1.6;
	}

	.contact-info {
		display: flex;
		justify-content: center;
		gap: 1rem;
		margin-top: 1rem;
	}

	a {
		color: #007bff;
		text-decoration: none;
		transition: color 0.3s ease;
	}

	a:hover {
		color: #0056b3;
	}
</style>