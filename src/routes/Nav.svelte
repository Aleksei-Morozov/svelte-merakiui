<script lang="ts">
	import { page } from '$app/stores';

	const components = [
		{ name: 'Label', href: '/label' },
		{ name: 'H1', href: '/h1' },
		{ name: 'Helper', href: '/helper' },
		{ name: 'Input', href: '/input' },
		{ name: 'Textarea', href: '/textarea' }
	];

	components.sort((a, b) => {
		if (a.name < b.name) return -1;
		return a.name > b.name ? 1 : 0;
	});

	const pluralize = (count: number, noun: string, suffix = 's') =>
		`${count} ${noun}${count !== 1 ? suffix : ''}`;
</script>

<nav {...$$props}>
	<header>
		{#if $page.route.id != '/'}
			<a href={'/'}>Svelte Meraki UI</a>
		{/if}
		<span>{pluralize(components.length, 'component')}</span>
	</header>
	<main>
		{#each components as component}
			<a href={component.href}>
				{component.name}
			</a>
		{/each}
	</main>
</nav>

<style lang="postcss">
	header {
		@apply mb-3 flex place-items-center gap-3;
	}
	header a {
		@apply text-lg font-medium text-gray-800 gdark:text-white;
	}
	span {
		@apply px-3 py-1 text-xs text-blue-600 bg-blue-100 rounded-full gdark:bg-gray-800 gdark:text-blue-400;
	}
	main {
		@apply flex items-center space-x-3 mb-8;
	}
	main a {
		@apply px-4 py-2 text-sm text-gray-800 transition-colors duration-300 bg-gray-100 rounded-lg hover:bg-gray-200;
	}
</style>
