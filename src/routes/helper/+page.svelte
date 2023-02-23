<script lang="ts">
	import Helper from '$lib/Helper.svelte';
	import H1 from '$lib/H1.svelte';
	import Section from '../Section.svelte';

	const code = `<Helper>Lorem ipsum dolor sit amet consectetur adipisicing elit.</Helper>`;
</script>

<H1>Helper</H1>

<Section heading="Helper text" {code}>
	<Helper>Lorem ipsum dolor sit amet consectetur adipisicing elit.</Helper>
</Section>
