<script lang="ts">
	import Highlight from 'svelte-highlight';
	import xml from 'svelte-highlight/languages/xml';
	import githubDark from 'svelte-highlight/styles/github-dark';

	export let code: string;
</script>

<svelte:head>
	{@html githubDark}
</svelte:head>

<Highlight language={xml} {code} class="lg:text-sm relative overflow-auto rounded-lg my-6 max-h-96" />
