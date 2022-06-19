<script>
	//  script for burger menu
	export let open = false;
	export let onClick = () => {
		open = !open;
		console.log(open);
	};
	export let ariaLabel = 'toggle menu';
</script>

<button
	on:click={onClick}
	aria-expanded={open}
	aria-label={ariaLabel}
	class="text-4xl w-10 h-10 flex justify-center items-center | lg:hidden"
>
	{#if open}
		<span class="text-green-300 hover:text-green-200 text-3xl"> &#10005; </span>
	{:else}
		<span class="text-green-300 hover:text-green-200">
			<img src="/svg/menu.svg" alt="" srcset="" />
		</span>
	{/if}
</button>
