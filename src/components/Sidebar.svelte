<script>
	let menu = [
		{ name: 'About', url: '/about' },
		{ name: 'Contact', url: '/contact' }
	];
	export let open = false;
</script>

<aside class="bg-blue-600" class:open>
	<ul>
		{#each menu as item}
			<li class="mx-1 mb-5">
				<a
					href={item.url}
					class="font-bold text-green-300 | hover:underline hover:text-green-200 transition"
					>{item.name}</a
				>
			</li>
		{/each}
	</ul>
</aside>
