<script lang="ts">
	const { ['class']: _, ...props } = $$restProps;
</script>

<!-- svelte-ignore a11y-mouse-events-have-key-events -->
<label class={$$restProps.class} {...props} on:mouseover on:mouseenter on:mouseleave>
	<slot />
</label>

<style lang="postcss">
	label {
		@apply mb-2 block text-sm text-gray-500 gdark:text-gray-300;
	}
</style>
