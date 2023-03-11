<script lang="ts">
	export let error: boolean = false;
</script>

<p class:error {...$$restProps}>
	<slot />
</p>

<style lang="postcss">
	p {
		@apply mt-3 text-xs text-gray-400 gdark:text-gray-600;
	}
	p.error {
		@apply text-red-400 gdark:text-red-400;
	}
</style>
