<script lang="ts">
	import Section from '../Section.svelte';
	import H1 from '$lib/H1.svelte';
	import Tabs from '$lib/Tabs.svelte';
	import Tab from '$lib/Tab.svelte';

	const links = [
		{ text: 'Profile' },
		{ text: 'Account' },
		{ text: 'Notification' },
		{ text: 'External', href: 'https://www.ietf.org/', target: '_blank' }
	];

	let code = `<script\>
	import { Tabs, Tab } from 'svelte-merakiui';

	const links = [
		{ text: 'Profile' },
		{ text: 'Account' },
		{ text: 'Notification' },
		{ text: 'External', href: 'https://www.ietf.org/', target: '_blank' }
	];
</script\>

<Tabs {links}>
	<Tab>Profile content</Tab>
	<Tab>Account content</Tab>
	<Tab>Notification content</Tab>
</Tabs>
`;
</script>

<H1>Tabs</H1>

<Section heading="Default" {code}>
	<Tabs {links}>
		<Tab>Profile content</Tab>
		<Tab>Account content</Tab>
		<Tab>Notification content</Tab>
	</Tabs>
</Section>
