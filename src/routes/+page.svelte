<script lang="ts">
	import Label from '$lib/Label.svelte';
	import Textarea from '$lib/Textarea.svelte';
</script>

<main>
	<h1>Svelte Meraki UI</h1>

	<section>
		<h2>Label</h2>
		<Label id="someId" text="This is label" />
	</section>

	<section>
		<h2>Textarea</h2>
		<Textarea
			label="Description"
			placeholder="Lorem ipsum..."
			message="Lorem ipsum dolor sit amet consectetur adipisicing elit."
		/>
	</section>
</main>

<style lang="postcss">
	main {
		@apply container py-10 px-4 mx-auto;
	}
	h1 {
		@apply text-2xl font-semibold text-gray-800 capitalize lg:text-3xl gdark:text-white mb-10;
	}
	section {
		@apply my-8;
	}
	h2 {
		@apply text-xl font-medium tracking-wide text-gray-700 mb-4;
	}
</style>
