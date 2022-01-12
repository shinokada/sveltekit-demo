<script>
	import { createEventDispatcher } from 'svelte';
	const dispatch = createEventDispatcher();

	export let url;
	export let name;

	function toggleSide() {
		dispatch('state', {
			open: false
		});
	}
</script>

<div class="border-b border-gray-400 mb-2 px-4">
	<a class="block" href="/{url}" on:click={toggleSide}>{name}</a>
</div>
