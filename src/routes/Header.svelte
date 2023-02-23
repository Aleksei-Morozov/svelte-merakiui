<script lang="ts">
	import { page } from '$app/stores';

	import Nav from './Nav.svelte';
</script>

{#if $page.route.id != '/'}
	<Nav />
{/if}
