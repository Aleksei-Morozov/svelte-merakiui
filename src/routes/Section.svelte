<script lang="ts">
	export let heading: string;
</script>

<h2>{heading}</h2>
<section>
	<slot />
</section>

<style lang="postcss">
	h2 {
		@apply mt-6 mb-4 text-xl font-medium tracking-wide text-gray-700;
	}
	section {
		@apply mb-8 px-16 py-16 rounded-lg bg-gray-100 gdark:bg-gray-900;
	}
</style>
