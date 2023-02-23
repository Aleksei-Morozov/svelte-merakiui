<script lang="ts">
	import { onMount } from 'svelte';

	type TabLink = {
		text: string;
		href?: string;
		target?: string;
	};

	export let active: number = 0;
	export let links: TabLink[] = [];

	let scope: Element;

	const open = (index: number): void => {
		active = index;

		if (!scope) return;
		scope.querySelectorAll('[role="tabpanel"]').forEach((node: Element, key: number) => {
			if (key != active) {
				node.classList.add('hidden');
			} else {
				node.classList.remove('hidden');
			}
		});
	};

	onMount(() => {
		open(active);
	});
</script>

<div bind:this={scope} role="navigation" {...$$restProps}>
	<div role="tablist">
		{#each links as link, key}
			{#if link.href}
				<a role="tab" class:active={active == key} href={link.href} target={link?.target}>
					{link.text}
				</a>
			{:else}
				<button role="tab" class:active={active == key} on:click={() => open(key)}>
					{link.text}
				</button>
			{/if}
		{/each}
	</div>
	<slot />
</div>

<style lang="postcss">
	[role='tablist'] {
		@apply flex overflow-x-auto overflow-y-hidden border-b border-gray-200 whitespace-nowrap gdark:border-gray-700;
	}
	[role='tab'] {
		@apply inline-flex items-center h-10 px-4 -mb-px text-sm text-center text-gray-700 bg-transparent border-b-2 border-transparent sm:text-base gdark:text-white whitespace-nowrap focus:outline-none hover:border-gray-400;
	}
	.active {
		@apply text-blue-600 border-blue-500 gdark:border-blue-400 gdark:text-blue-300;
	}
</style>
