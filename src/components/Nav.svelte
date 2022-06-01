<script>
    let menu = [
        { name: 'About', url: '/about' },
        { name: 'Contact', url: '/contact'}
    ];
</script>

<nav>
    <div class="navbar">
        <a href="/" class="font-bold text-xl text-green-300 | hover:text-green-200 transition">SpinUp Labs x Svelte/TW</a>
        <!-- DT menu -->
        <ul class="hidden lg:flex">
            {#each menu as item}
            <li class="mx-1"><a href={item.url} class="font-bold text-green-300 | hover:underline hover:text-green-200 transition">{item.name}</a></li>
            {/each}
        </ul>
    
        <div class="burger-container">
            <input type="checkbox" class="checkbox"/>
            <div class="burger">
                <span class="line line-1"></span>
                <span class="line line-2"></span>
                <span class="line line-3"></span>
            </div>
            <!-- Mobile menu -->
            <ul class="menu-items">
                {#each menu as item}
                <li class="mx-1 mb-5"><a href={item.url} class="font-bold text-green-300 | hover:underline hover:text-green-200 transition">{item.name}</a></li>
                {/each}
            </ul>
        </div>
    </div>
</nav>