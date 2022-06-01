<script>
    let shown = false;
    export function toggle(){
        shown = !shown
    }
</script>

{#if shown}
<div class="bg-blue-500 bg-opacity-50 fixed w-full h-full top-0 left-0 text-center text-blue-600">
    <div class="border-2 border-blue-500 rounded-2xl bg-slate-100 max-w-4xl p-5 mx-auto my-20">
        <button on:click={() => toggle()} class="rounded-full border border-blue-500 px-3.5 py-2 font-extrabold text-lg transition | hover:bg-blue-500 hover:text-green-300">&#10005;</button>
        <slot>Modal Content goes here</slot>
    </div>
</div>
{/if}