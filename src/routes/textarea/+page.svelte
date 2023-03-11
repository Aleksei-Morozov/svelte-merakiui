<script lang="ts">
	import Section from '../Section.svelte';
	import Textarea from '$lib/Textarea.svelte';
	import Label from '$lib/Label.svelte';
	import H1 from '$lib/H1.svelte';
	import Helper from '$lib/Helper.svelte';
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

<H1>Textarea</H1>

<Tabs {links} class="mt-4">
	<Tab>
		<Section heading="Default textarea" code={`<Textarea placeholder="Lorem ipsum..." />`}>
			<Textarea placeholder="Lorem ipsum..." />
		</Section>
	</Tab>
	<Tab>
		<Section heading="Disabled textarea" code={`<Textarea disabled placeholder="Lorem ipsum..." />`}>
			<Textarea disabled placeholder="Lorem ipsum..." />
		</Section>
	</Tab>
	<Tab>
		<Section
			heading="Textarea with label"
			code={'<Textarea label="Description" placeholder="Lorem ipsum..." />'}
		>
			<Textarea label="Description" placeholder="Lorem ipsum..." />
		</Section>
	</Tab>
	<Tab>
		<Section
			heading="Textarea with label and helper text"
			code={`<Textarea
	label="Description"
	helper="Lorem ipsum dolor sit amet consectetur adipisicing elit."
	placeholder="Lorem ipsum..."
/>`}
		>
			<Textarea
				label="Description"
				helper="Lorem ipsum dolor sit amet consectetur adipisicing elit."
				placeholder="Lorem ipsum..."
			/>
		</Section>
	</Tab>
	<Tab>
		<Section
			heading="Textarea with label and error message"
			code={`<Textarea
	label="Description"
	error
	helper="Lorem ipsum dolor sit amet consectetur adipisicing elit."
	placeholder="Lorem ipsum..."
/>`}
		>
			<Textarea
				label="Description"
				error
				helper="Lorem ipsum dolor sit amet consectetur adipisicing elit."
				placeholder="Lorem ipsum..."
			/>
		</Section>
	</Tab>
</Tabs>
