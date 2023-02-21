<script lang="ts">
	export let label: string = '';
	export let placeholder: string = '';
	export let message: string = '';

	const id: string = Math.random().toString(36).substring(2, 11);
</script>

<div>
	<label for={id}>{label}</label>
	<textarea {id} {placeholder} {...$$restProps} />
	<p>{message}</p>
</div>

<style lang="postcss">
	label {
		@apply block text-sm text-gray-500 gdark:text-gray-300;
	}
	textarea {
		@apply block mt-2 w-full placeholder-gray-400/70 gdark:placeholder-gray-500 rounded-lg border border-gray-200 bg-white px-4 h-32 py-2.5 text-gray-700 focus:border-blue-400 focus:outline-none focus:ring focus:ring-blue-300 focus:ring-opacity-40 gdark:border-gray-600 gdark:bg-gray-900 gdark:text-gray-300 gdark:focus:border-blue-300;
	}
	p {
		@apply mt-3 text-xs text-gray-400 gdark:text-gray-600;
	}
</style>
