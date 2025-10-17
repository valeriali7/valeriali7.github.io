<script lang="ts">
	import Hero from '$lib/components/Hero.svelte';
	import Research from '$lib/components/Research.svelte';
	import Experience from '$lib/components/Experience.svelte';
	import Publications from '$lib/components/Publications.svelte';
	import Presentations from '$lib/components/Presentations.svelte';

	let darkMode = $state(false);
	let mobileMenuOpen = $state(false);

	function toggleDarkMode() {
		darkMode = !darkMode;
	}

	function toggleMobileMenu() {
		mobileMenuOpen = !mobileMenuOpen;
	}

	function closeMobileMenu() {
		mobileMenuOpen = false;
	}
</script>

<nav class:dark={darkMode}>
	<div class="nav-container">
		<button class="hamburger" onclick={toggleMobileMenu} aria-label="Toggle menu">
			<span></span>
			<span></span>
			<span></span>
		</button>
		<div class="nav-links" class:open={mobileMenuOpen}>
			<a href="#about" onclick={closeMobileMenu}>About</a>
			<a href="#publications" onclick={closeMobileMenu}>Publications</a>
			<a href="#presentations" onclick={closeMobileMenu}>Presentations</a>
			<!-- <a href="#research" onclick={closeMobileMenu}>Research</a> -->
			<a href="#experience" onclick={closeMobileMenu}>Experience</a>
		</div>
		<button class="theme-toggle" onclick={toggleDarkMode}>
			{darkMode ? '☀︎':'⏾⋆.˚'}
		</button>
	</div>
</nav>

<main class:dark={darkMode}>
	<Hero />
	<Publications />
	<Presentations />
	<!-- deleting cuz it look stoopid <Research /> -->
	<Experience />
</main>

<style>
	/* Navigation */
	nav {
		position: sticky;
		top: 0;
		background-color: #ffffff;
		z-index: 100;
		transition: background-color 0.3s ease;
	}

	nav.dark {
		background-color: #1e293b;
	}

	.nav-container {
		max-width: 900px;
		margin: 0 auto;
		padding: 1rem 2rem;
		display: flex;
		justify-content: space-between;
		align-items: center;
		position: relative;
	}

	.hamburger {
		display: none;
		flex-direction: column;
		gap: 4px;
		background: none;
		border: none;
		cursor: pointer;
		padding: 0.5rem;
	}

	.hamburger span {
		width: 24px;
		height: 2px;
		background-color: #475569;
		transition: background-color 0.3s ease;
	}

	nav.dark .hamburger span {
		background-color: #94a3b8;
	}

	.nav-links {
		display: flex;
		gap: 2rem;
	}

	.nav-links a {
		font-size: 1.25rem;
		font-weight: 500;
		color: #475569;
		transition: color 0.2s ease;
		text-decoration: none;
	}

	.nav-links a:hover {
		color: #0f172a;
	}

	nav.dark .nav-links a {
		color: #94a3b8;
	}

	nav.dark .nav-links a:hover {
		color: #f1f5f9;
	}

	.theme-toggle {
		background: none;
		border: 1px solid #e2e8f0;
		padding: 0.5rem 0.75rem;
		cursor: pointer;
		font-size: 1.25rem;
		border-radius: 6px;
		transition: opacity 0.2s ease, border-color 0.3s ease, background-color 0.3s ease;
	}

	.theme-toggle:hover {
		background-color: #f1f5f9;
	}

	nav.dark .theme-toggle {
		border-color: #475569;
	}

	nav.dark .theme-toggle:hover {
		background-color: #334155;
	}

	main {
		width: 100%;
		transition: background-color 0.3s ease, color 0.3s ease;
	}

	main.dark {
		background-color: #0f172a;
		color: #f1f5f9;
	}

	/* Responsive Design */
	@media (max-width: 768px) {
		.hamburger {
			display: flex;
		}

		.nav-container {
			padding: 0.75rem 1rem;
		}

		.nav-links {
			position: fixed;
			top: 57px;
			left: 0;
			right: 0;
			flex-direction: column;
			gap: 0;
			background-color: #ffffff;
			padding: 0;
			max-height: 0;
			overflow: hidden;
			transition: max-height 0.3s ease, padding 0.3s ease;
		}

		nav.dark .nav-links {
			background-color: #1e293b;
		}

		.nav-links.open {
			max-height: 300px;
			padding: 1rem 0;
		}

		.nav-links a {
			padding: 0.75rem 1.5rem;
			font-size: 0.9rem;
			border-bottom: 1px solid #f1f5f9;
		}

		nav.dark .nav-links a {
			border-bottom-color: #334155;
		}

		.nav-links a:last-child {
			border-bottom: none;
		}

		.theme-toggle {
			padding: 0.4rem 0.6rem;
			font-size: 1.1rem;
		}
	}
</style>
