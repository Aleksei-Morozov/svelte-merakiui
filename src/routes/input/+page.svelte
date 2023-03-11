<script lang="ts">
	import Input from '$lib/Input.svelte';
	import Label from '$lib/Label.svelte';
	import Helper from '$lib/Helper.svelte';
	import H1 from '$lib/H1.svelte';
	import Section from '../Section.svelte';
	import Tabs from '$lib/Tabs.svelte';
	import Tab from '$lib/Tab.svelte';

	const links = [
		{ text: 'Default' },
		{ text: 'Disabled' },
		{ text: 'With label' },
		{ text: 'With label & helper' },
		{ text: 'With label & error' }
	];
</script>

<H1>Input</H1>

<Tabs {links} class="mt-4">
	<Tab>
		<Section heading="Default text input" code={'<Input placeholder="John Doe" />'}>
			<Input placeholder="John Doe" />
		</Section>
	</Tab>
	<Tab>
		<Section heading="Input disabled" code={'<Input disabled placeholder="John Doe" />'}>
			<Input disabled placeholder="John Doe" />
		</Section>
	</Tab>
	<Tab>
		<Section
			heading="Input with label"
			code={'<Label for="input1" class="mb-2">Username</Label>\n<Input id="input1" placeholder="John Doe" />'}
		>
			<Label for="input1" class="mb-2">Username</Label>
			<Input id="input1" placeholder="John Doe" />
		</Section>
	</Tab>
	<Tab>
		<Section
			heading="Input with label and helper text"
			code={`<Input
	label="Username"
	helper="Lorem ipsum dolor sit amet consectetur adipisicing elit."
	placeholder="John Doe"
/>`}
		>
			<Input
				label="Username"
				helper="Lorem ipsum dolor sit amet consectetur adipisicing elit."
				placeholder="John Doe"
			/>
		</Section>
		<Section
			heading="Input with label and helper text"
			code={`<Label for="input2">Username</Label>
<Input id="input2" placeholder="John Doe" />
<Helper>Lorem ipsum dolor sit amet consectetur adipisicing elit.</Helper>`}
		>
			<Label for="input2">Username</Label>
			<Input id="input2" placeholder="John Doe" />
			<Helper>Lorem ipsum dolor sit amet consectetur adipisicing elit.</Helper>
		</Section>
	</Tab>
	<Tab>
		<Section
			heading="Input with label and error message"
			code={'<Label for="input3">Username</Label>\n<Input error id="input3" placeholder="John Doe" />\n<Helper error class="mt-3">Lorem ipsum dolor sit amet consectetur adipisicing elit.</Helper>'}
		>
			<Label for="input3">Username</Label>
			<Input error id="input3" placeholder="John Doe" />
			<Helper error class="mt-3">Lorem ipsum dolor sit amet consectetur adipisicing elit.</Helper>
		</Section>
	</Tab>
</Tabs>
