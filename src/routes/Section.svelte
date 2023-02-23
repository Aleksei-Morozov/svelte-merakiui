<script lang="ts">
	import Code from './Code.svelte';

	export let heading: string = '';
	export let code: string = '';
</script>

<section>
	{#if heading}
		<h2>{heading}</h2>
	{/if}

	<div {...$$restProps}>
		<slot />
	</div>

	{#if code}
		<Code {code} />
	{/if}
</section>

<style lang="postcss">
	section {
		@apply my-2;
	}
	h2 {
		@apply mb-4 text-xl font-medium tracking-wide text-gray-700;
	}
	div {
		@apply mb-6 px-16 py-16 rounded-lg bg-gray-100 gdark:bg-gray-900;
	}
</style>
