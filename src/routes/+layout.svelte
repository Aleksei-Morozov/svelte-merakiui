<script>
	import '../app.postcss';
	import Nav from './Nav.svelte';
	import { page } from '$app/stores';
</script>

<main>
	<h1>
		{#if $page.route.id != '/'}
			<a href={'/'}>Svelte Meraki UI</a>
		{:else}
			Svelte Meraki UI
		{/if}
	</h1>

	<Nav />

	<slot />
</main>

<style lang="postcss">
	main {
		@apply container py-10 px-4 mx-auto;
	}
	h1 {
		@apply text-2xl font-semibold text-gray-800 capitalize lg:text-3xl gdark:text-white mb-10;
	}
</style>
