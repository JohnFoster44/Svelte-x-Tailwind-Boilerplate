<script>
    let menu = [
        { name: 'About', url: '/about' },
        { name: 'Contact', url: '/contact'}
    ];
</script>

<footer class="flex bg-blue-600 text-lg font-bold p-5 mt-auto">
    <p class="text-green-400">Footer:</p>
    <ul class="flex">
        {#each menu as item}
            <li class="mx-2 "><a href={item.url} class="text-green-300 | hover:underline hover:text-green-200 transition">{item.name}</a></li>
        {/each}
    </ul>
</footer>