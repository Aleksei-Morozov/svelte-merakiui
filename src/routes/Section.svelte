<script lang="ts">
	import Code from './Code.svelte';

	export let heading: string;
	export let code: string = '';
</script>

<section>
	<h2>{heading}</h2>
	
	<div {...$$restProps}>
		<slot />
	</div>
	
	{#if code}
		<Code {code} />
	{/if}
</section>

<style lang="postcss">
	section {
		@apply mb-10;
	}
	h2 {
		@apply mt-6 mb-4 text-xl font-medium tracking-wide text-gray-700;
	}
	div {
		@apply mb-6 px-16 py-16 rounded-lg bg-gray-100 gdark:bg-gray-900;
	}
</style>
