<script lang="ts">
	const components = [
		{ name: 'Label', href: '/label' },
		{ name: 'Helper', href: '/helper' },
		{ name: 'Input', href: '/input' },
		{ name: 'Textarea', href: '/textarea' }
	];
</script>

<div>
	<span>{components.length} components</span>
</div>
<nav>
	{#each components as component}
		<a href={component.href}>
			{component.name}
		</a>
	{/each}
</nav>

<style lang="postcss">
	span {
		@apply px-3 py-1 text-xs text-blue-600 bg-blue-100 rounded-full dark:bg-gray-800 dark:text-blue-400;
	}
	nav {
		@apply flex items-center space-x-3 mt-4 mb-8;
	}
	a {
		@apply px-4 py-2 text-sm text-gray-800 transition-colors duration-300 bg-gray-100 rounded-lg hover:bg-gray-200;
	}
</style>
