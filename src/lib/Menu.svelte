<script>
    import { page } from '$app/stores'
    $: active = $page.url.pathname;
    
    let items = [
        {
            slug: '/',
            name: 'Home',
        },{
            slug: '/datenschutz/',
            name: 'Datenschutz',
        },{
            slug: '/impressum',
            name: 'Impressum',
        },
    ]
</script>


<nav>
    <ul>
        {#each items as {slug, name}}
        <li>
            <a
            sveltekit:prefetch href="{slug}"
            on:click={()=>{active=slug}}
            class:active={active === slug}
            >
                {name}
            </a>
        </li>
        {/each}
    </ul>
</nav>

<style>
    nav {
        width: max-content;
        margin:auto;
    }
    ul {
        list-style-type: none;
        display: flex;
    }
    a {
        margin: .5em;
        padding: .5em;
        text-decoration: none;
    }
    a:hover {
        background: rgba(0,0,0,.1);
    }
    a.active {
        background: rgba(0,0,0,.2);
    }

</style>