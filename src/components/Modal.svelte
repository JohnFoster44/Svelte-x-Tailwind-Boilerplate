<script>
    let shown = false;
    export function toggle(){
        shown = !shown
    }
</script>

{#if shown}
<!-- Background -->
<div class="bg-blue-500 bg-opacity-50 fixed w-full h-full top-0 left-0" on:click={() => toggle()}></div>
<!-- Modal -->
<div class="border-2 border-blue-500 rounded-2xl bg-slate-100 max-w-4xl p-5 mx-auto my-20 translate-y-1/2 text-center text-blue-600 container">
    <div class="absolute right-0 mx-5"><button on:click={() => toggle()} class="rounded-full border border-blue-600 px-3.5 py-2 font-extrabold text-lg transition | hover:bg-blue-600 hover:text-green-300">&#10005;</button></div>
    <slot>Modal Content goes here</slot>
</div>
{/if}