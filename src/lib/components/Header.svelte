<script>
	let currentSection = '';

	function updateCurrentSection() {
		const sections = document.querySelectorAll('section');
		const scrollPosition = window.scrollY;

		for (let section of sections) {
			if (section.offsetTop <= scrollPosition + 100) {
				currentSection = section.id;
			}
		}
	}

	if (typeof window !== 'undefined') {
		window.addEventListener('scroll', updateCurrentSection);
	}
</script>

<header>
	<nav>
		<ul>
			<li class:active={currentSection === 'introduction'}><a href="#introduction">Welcome</a></li>
			<li class:active={currentSection === 'projects'}><a href="#projects">Projects</a></li>
			<li class:active={currentSection === 'skills'}><a href="#skills">Skills</a></li>
			<li class:active={currentSection === 'experiences'}><a href="#experiences">Experience</a></li>
		</ul>
	</nav>
</header>

<style>
	header {
		background-color: #343a40;
		padding: 1rem;
		position: sticky;
		top: 0;
		z-index: 100;
	}

	nav ul {
		display: flex;
		justify-content: center;
		list-style-type: none;
		padding: 0;
		margin: 0;
	}

	nav li {
		margin: 0 1rem;
	}

	nav a {
		color: #fff;
		text-decoration: none;
		font-weight: bold;
		transition: color 0.3s ease;
	}

	nav a:hover, nav li.active a {
		color: #007bff;
	}
</style>