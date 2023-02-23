<script lang="ts">
	import Section from '../Section.svelte';
	import Input from '$lib/Input.svelte';
	import Label from '$lib/Label.svelte';
	import Helper from '$lib/Helper.svelte';
	import H1 from '$lib/H1.svelte';
</script>

<H1>Input</H1>

<Section heading="Single input">
	<Input placeholder="John Doe" />
</Section>

<Section heading="Input disabled">
	<Input disabled placeholder="John Doe" />
</Section>

<Section heading="Input with label">
	<Label for="input1">Username</Label>
	<Input id="input1" placeholder="John Doe" />
</Section>

<Section heading="Input with label and helper text">
	<Label for="input2">Username</Label>
	<Input id="input2" placeholder="John Doe" />
	<Helper>Lorem ipsum dolor sit amet consectetur adipisicing elit.</Helper>
</Section>

<Section heading="Input with label and error message">
	<Label for="input3">Username</Label>
	<Input error id="input3" placeholder="John Doe" />
	<Helper error>Lorem ipsum dolor sit amet consectetur adipisicing elit.</Helper>
</Section>
