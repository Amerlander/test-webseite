<script>
    import Header from "$lib/Header.svelte"
    import Footer from "$lib/Footer.svelte"
    import '../global.css'
    import '../fonts.css'
</script>

<Header />

<main>
    <slot />
</main>

<Footer />