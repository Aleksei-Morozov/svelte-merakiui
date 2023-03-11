<script lang="ts">
	import Label from './Label.svelte';
	import Helper from './Helper.svelte';

	export let value: string = '';
	export let label: string = '';
	export let helper: string = '';
	export let error: boolean = false;
	export let disabled: boolean = false;

	export let id = label ? Math.random().toString(36).slice(2) : undefined;
</script>

{#if label}
	<Label for={id}>{label}</Label>
{/if}

<textarea
	{id}
	class:error
	bind:value
	{disabled}
	{...$$restProps}
	on:blur
	on:change
	on:click
	on:contextmenu
	on:input
	on:focus
	on:keydown
	on:keypress
	on:keyup
	on:mouseenter
	on:mouseleave
	on:mouseover
	on:paste
/>

{#if helper}
	<Helper {error}>{helper}</Helper>
{/if}

<style lang="postcss">
	textarea {
		@apply block w-full placeholder-gray-400/70 gdark:placeholder-gray-500 rounded-lg border border-gray-200 bg-white px-5 py-2.5 text-gray-700 focus:border-blue-400 focus:outline-none focus:ring focus:ring-blue-300 focus:ring-opacity-40 gdark:border-gray-600 gdark:bg-gray-900 gdark:text-gray-300 gdark:focus:border-blue-300;
	}

	.error {
		@apply gdark:placeholder-gray-500 border-red-400 focus:border-red-400 focus:ring-red-300 focus:ring-opacity-40 gdark:border-red-400 gdark:focus:border-red-300;
	}

	textarea:disabled {
		@apply bg-gray-50 cursor-not-allowed;
	}
</style>
