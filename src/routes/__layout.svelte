<script>
	import Header from '$lib/header/Header.svelte';
	import Overlay from '../components/Overlay.svelte';
	import '../app.css';
	import { isOverlayOpen } from '../stores/OverlayStore';
</script>

<Header />

{#if $isOverlayOpen}
	<Overlay>
		<h1 class="text-white text-4xl">OVERLAY!!!</h1>
		<p class="text-white text-center">This is pretty cool!</p>
	</Overlay>
{/if}
<main>
	<slot />
</main>

<footer>
	<p>visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to learn SvelteKit</p>
</footer>

<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 1024px;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 40px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 40px 0;
		}
	}
</style>
