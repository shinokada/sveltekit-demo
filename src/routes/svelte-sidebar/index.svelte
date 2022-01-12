<script>
	import { Sidebar } from '@codewithshin/svelte-sidebar';
	let lists = [
		{ url: 'svelte-sidebar', name: 'Svelte-sidebar Home' },
		{ url: 'svelte-sidebar/default', name: 'Sidebar Default' },
		{ url: 'svelte-sidebar/custom', name: 'Sidebar Custom Style' },
		{ url: 'svelte-sidebar/multi-default', name: 'Multi-menu Default' },
		{ url: 'svelte-sidebar/multi-custom', name: 'Multip-menu Custom Style' }
	];
	let siteName = 'Svelte-sidebar Demo';
</script>

<Sidebar {lists} {siteName} />
<main class="container mx-auto">
	<h1>
		{siteName}
	</h1>
</main>
