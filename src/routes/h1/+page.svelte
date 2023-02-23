<script lang="ts">
	import H1 from '$lib/H1.svelte';
	import Section from '../Section.svelte';

	const code = `<H1>Heading</H1>`;
</script>

<H1>H1</H1>

<Section heading="H1 heading" {code}>
	<H1>Heading</H1>
</Section>
