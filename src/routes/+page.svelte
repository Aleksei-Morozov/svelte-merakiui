<script lang="ts">
	import Nav from './Nav.svelte';
</script>

<h1>Svelte Meraki UI</h1>

<p>Svelte component library for Meraki UI.</p>

<Nav class="mt-8" />

<style lang="postcss">
	h1 {
		@apply text-2xl font-semibold text-gray-800 capitalize lg:text-3xl gdark:text-white mb-6;
	}
	p {
		@apply text-gray-500 dark:text-gray-400;
	}
</style>
