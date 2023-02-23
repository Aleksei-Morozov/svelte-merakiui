<script lang="ts">
	import Section from '../Section.svelte';
	import Textarea from '$lib/Textarea.svelte';
	import Label from '$lib/Label.svelte';
	import H1 from '$lib/H1.svelte';
	import Helper from '$lib/Helper.svelte';
</script>

<H1>Textarea</H1>

<Section heading="Single textarea">
	<Textarea placeholder="Lorem ipsum..." />
</Section>

<Section heading="Textarea with label">
	<Label for="textarea1">Description</Label>
	<Textarea id="textarea1" placeholder="Lorem ipsum..." />
</Section>

<Section heading="Textarea with label and helper text">
	<Label for="textarea2">Description</Label>
	<Textarea id="textarea2" placeholder="Lorem ipsum..." />
	<Helper>Lorem ipsum dolor sit amet consectetur adipisicing elit.</Helper>
</Section>

<Section heading="Textarea with label and error message">
	<Label for="textarea3">Description</Label>
	<Textarea error id="textarea3" placeholder="Lorem ipsum..." />
	<Helper error>Lorem ipsum dolor sit amet consectetur adipisicing elit.</Helper>
</Section>
