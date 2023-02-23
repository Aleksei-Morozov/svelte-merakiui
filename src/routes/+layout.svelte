<script>
	import '../app.postcss';
	import Header from './Header.svelte';
</script>

<main>
	<Header />
	<slot />
</main>

<style lang="postcss">
	main {
		@apply container py-8 px-4 mx-auto;
	}
</style>
