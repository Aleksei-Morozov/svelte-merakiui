<script lang="ts">
	import Section from '../Section.svelte';
	import H1 from '$lib/H1.svelte';
	import Tabs from '$lib/Tabs.svelte';
	import Tab from '$lib/Tab.svelte';
</script>

<H1>Tabs</H1>

<Section
	heading="Default"
	code={`<Tabs labels=\{['Profile', 'Account', 'Notification']\}>\n\t<Tab>Profile content</Tab>\n\t<Tab>Account content</Tab>\n\t<Tab>Notification content</Tab>\n</Tabs>`}
>
	<Tabs labels={['Profile', 'Account', 'Notification']}>
		<Tab>Profile content</Tab>
		<Tab>Account content</Tab>
		<Tab>Notification content</Tab>
	</Tabs>
</Section>
