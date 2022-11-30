<script>
    let zahl = 3;
    let name = "world"
    $: doppelt = zahl * 2;
    $: console.log(zahl, doppelt);
</script>

<h1>Hello {name}</h1>

<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
<p>Visit <a href="https://kigfdgft.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<input type="number" bind:value={zahl} />

<div style="height:{doppelt}px;"></div>

<input type="text" bind:value={name} />

{doppelt}

<style>
    div {
        width: 100%;
        background: orange;
    }
    a {
      color: red;
    }
    a:visited {
        color: green;
    }

    input {
        font-size: 1.4em;
        background: rgb(255,200,230);
        color: red;
        padding: .5em;
        border-radius: 5px;
        border: none;
        margin: 5px;
    }
</style>