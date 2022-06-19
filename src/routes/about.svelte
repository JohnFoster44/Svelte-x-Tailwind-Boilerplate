<script>
	import Modal from '../components/Modal.svelte';
	let modal;
</script>

<main class="container mx-auto">
	<div class="text-center text-blue-600">
		<h1 class="text-3xl font-bold">About page</h1>
		<span>~</span>
		<h3 class="font-bold mb-5">a simple page nothing much to see here</h3>
		<button
			class="p-5 bg-blue-600 text-green-300 font-bold text-lg rounded-xl | hover:bg-blue-700 active:bg-blue-800 hover:text-green-300"
			on:click={() => modal.toggle()}>Modal</button
		>
	</div>
</main>

<Modal bind:this={modal}>
	<div class="mb-10">
		<h1 class="text-3xl font-bold mb-5">Modal</h1>
		<span>~</span>
	</div>
	<p>boo yahhh</p>
</Modal>
