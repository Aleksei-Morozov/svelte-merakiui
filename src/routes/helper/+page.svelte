<script lang="ts">
	import Helper from '$lib/Helper.svelte';
	import H1 from '$lib/H1.svelte';
	import Section from '../Section.svelte';
</script>

<H1>Helper</H1>

<Section
	heading="Helper text"
	code={'<Helper>Lorem ipsum dolor sit amet consectetur adipisicing elit.</Helper>'}
>
	<Helper>Lorem ipsum dolor sit amet consectetur adipisicing elit.</Helper>
</Section>

<Section
	heading="Error message"
	code={'<Helper error>Lorem ipsum dolor sit amet consectetur adipisicing elit.</Helper>'}
/>
