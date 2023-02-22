<script lang="ts">
	export let id: string;
	export let text: string = '';
</script>

{#if text}
	<label for={id}>{text}</label>
{/if}

<style lang="postcss">
	label {
		@apply block text-sm text-gray-500 gdark:text-gray-300;
	}
</style>
