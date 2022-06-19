<script>
	import BurgerMenu from '../components/BurgerMenu.svelte';
	import { fly } from 'svelte/transition';
	let menu = [
		{ name: 'About', url: '/about' },
		{ name: 'Contact', url: '/contact' }
	];
	let open;
</script>

<header>
	<div class="navbar">
		<a href="/" class="font-bold text-xl text-green-300 | hover:text-green-200 transition"
			>SpinUp Labs x Svelte/TW</a
		>
		<!-- DT menu -->
		<nav>
			<ul class="hidden lg:flex">
				{#each menu as item}
					<li class="mx-1">
						<a
							href={item.url}
							class="font-bold text-green-300 | hover:underline hover:text-green-200 transition"
							>{item.name}</a
						>
					</li>
				{/each}
			</ul>
		</nav>
		<BurgerMenu bind:open />
	</div>
	{#if open}
		<nav
			class="bg-blue-600 absolute top-0 h-screen w-full text-center text-4xl overflow-hidden pt-10"
			transition:fly={{ x: 150, duration: 150 }}
		>
			<ul>
				<li class="mb-5">
					<a
						href="/"
						class="font-bold text-green-300 | hover:underline hover:text-green-200 transition"
						on:click={() => (open = !open)}>Home</a
					>
				</li>
				{#each menu as item}
					<li class="mb-5">
						<a
							href={item.url}
							class="font-bold text-green-300 | hover:underline hover:text-green-200 transition"
							on:click={() => (open = !open)}>{item.name}</a
						>
					</li>
				{/each}
			</ul>
		</nav>
	{/if}
</header>
