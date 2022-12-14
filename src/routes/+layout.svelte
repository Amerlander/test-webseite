<script>
    import '$lib/../css/global.css'
    import '$lib/../css/fonts.css'
    
    import Header from "$lib/Header.svelte"
    import Footer from "$lib/Footer.svelte"

</script>

<Header />

<main>
    <slot />
</main>

<Footer />