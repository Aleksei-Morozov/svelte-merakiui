<script lang="ts">
	const { ['class']: _, ...props } = $$restProps;
</script>

<label class={$$restProps.class} {...props}>
	<slot />
</label>

<style lang="postcss">
	label {
		@apply block text-sm text-gray-500 gdark:text-gray-300;
	}
</style>
