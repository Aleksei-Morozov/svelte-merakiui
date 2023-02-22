<script lang="ts">
	import Label from '$lib/Label.svelte';
	import Textarea from '$lib/Textarea.svelte';
	import Helper from '$lib/Helper.svelte';
</script>

<main>
	<h1>Svelte Meraki UI</h1>

	<h2>Label</h2>
	<section>
		<Label for="someId">Lorem ipsum</Label>
	</section>

	<h2>Helper</h2>
	<section>
		<Helper>Lorem ipsum dolor sit amet consectetur adipisicing elit.</Helper>
	</section>

	<h2>Textarea</h2>
	<section>
		<Textarea placeholder="Lorem ipsum..." />
	</section>

	<h2>Textarea with label</h2>
	<section>
		<Label for="myTextarea1">Description</Label>
		<Textarea id="myTextarea1" placeholder="Lorem ipsum..." />
	</section>

	<h2>Textarea with label and helper text</h2>
	<section>
		<Label for="myTextarea2">Description</Label>
		<Textarea id="myTextarea2" placeholder="Lorem ipsum..." />
		<Helper>Lorem ipsum dolor sit amet consectetur adipisicing elit.</Helper>
	</section>

	<h2>Textarea with label and error message</h2>
	<section>
		<Label for="myTextarea3">Description</Label>
		<Textarea error id="myTextarea3" placeholder="Lorem ipsum..." />
		<Helper error>Lorem ipsum dolor sit amet consectetur adipisicing elit.</Helper>
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
		@apply mb-8 p-4 rounded-lg bg-gray-100 gdark:bg-gray-900;
	}
	h2 {
		@apply mb-4 text-xl font-medium tracking-wide text-gray-700;
	}
</style>
