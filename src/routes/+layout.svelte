<script lang="ts">
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children?.()}

<style>
	:global(*) {
		margin: 0;
		padding: 0;
		box-sizing: border-box;
	}

	:global(body) {
		font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
		line-height: 1.6;
		color: #1e293b;
		background-color: #f8fafc;
		min-height: 100vh;
	}

	:global(h1) {
		font-size: clamp(2rem, 5vw, 3rem);
		font-weight: 700;
		color: #0f172a;
		margin-bottom: 0.5rem;
		letter-spacing: -0.02em;
		transition: color 0.3s ease;
	}

	:global(main.dark h1) {
		color: #f1f5f9;
	}

	:global(h2) {
		font-size: clamp(1.5rem, 4vw, 2rem);
		font-weight: 600;
		color: #0f172a;
		margin-bottom: 2rem;
		letter-spacing: -0.01em;
		transition: color 0.3s ease;
	}

	:global(main.dark h2) {
		color: #f1f5f9;
	}

	:global(h3) {
		font-size: clamp(1.125rem, 3vw, 1.375rem);
		font-weight: 600;
		color: #334155;
		margin-bottom: 0.5rem;
		transition: color 0.3s ease;
	}

	:global(main.dark h3) {
		color: #cbd5e1;
	}

	:global(p) {
		margin-bottom: 1rem;
		color: #475569;
		font-size: 1rem;
		transition: color 0.3s ease;
	}

	:global(main.dark p) {
		color: #94a3b8;
	}

	:global(a) {
		color: #334155;
		text-decoration: none;
		transition: opacity 0.2s ease, color 0.3s ease;
	}

	:global(a:hover) {
		opacity: 0.6;
	}

	:global(main.dark a) {
		color: #cbd5e1;
	}

	:global(html) {
		scroll-behavior: smooth;
	}
</style>
