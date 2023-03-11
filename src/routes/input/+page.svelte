<script lang="ts">
	import { Input, Label, Helper, H1 } from '$lib/index.js';
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
		<Section heading="Disabled input" code={'<Input disabled placeholder="John Doe" />'}>
			<Input disabled placeholder="John Doe" />
		</Section>
	</Tab>
	<Tab>
		<Section heading="Input with label" code={'<Input label="Username" placeholder="John Doe" />'}>
			<Input label="Username" placeholder="John Doe" />
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
	</Tab>
	<Tab>
		<Section
			heading="Input with label and error message"
			code={`<Input
	label="Username"
	error
	helper="Lorem ipsum dolor sit amet consectetur adipisicing elit."
	placeholder="John Doe"
/>`}
		>
			<Input
				label="Username"
				error
				helper="Lorem ipsum dolor sit amet consectetur adipisicing elit."
				placeholder="John Doe"
			/>
		</Section>
	</Tab>
</Tabs>
