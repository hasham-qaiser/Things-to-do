<script>
	import { text } from 'svelte/internal';

	export let todos;
</script>

<div class="rounded-lg shadow-lg p-8 flex flex-col gap-4">
	{#each todos as item, index}
		<div class="rounded-md p-3 justify-between flex flex-row border-2 border-gray-800">
			<div class="font-medium text-sm">{item.text}</div>
			<button class="font-light text-sm">remove</button>
		</div>
	{/each}
</div>
