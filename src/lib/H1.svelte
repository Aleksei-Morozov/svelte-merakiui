<h1 {...$$props}>
	<slot />
</h1>

<style lang="postcss">
	h1 {
		@apply font-semibold text-2xl lg:text-3xl 2xl:text-4xl text-gray-800 gdark:text-white;
	}
</style>
