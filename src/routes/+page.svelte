<script lang="ts">
	import Label from '$lib/Label.svelte';
	import Textarea from '$lib/Textarea.svelte';
</script>

<main>
	<h1>Svelte Meraki UI</h1>

	<h2>Label</h2>
	<section>
		<Label id="someId" text="This is label" />
	</section>

	<h2>Textarea</h2>
	<section>
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
		@apply mb-8 p-4 rounded-lg bg-gray-100 dark:bg-gray-900;

	}
	h2 {
		@apply mb-4 text-xl font-medium tracking-wide text-gray-700;
	}
</style>
