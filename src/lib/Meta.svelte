<script>
    export let title = '';
    export let description = '';
</script>

<svelte:head>
	<title>{title} | Freie Schule Roddahn</title>
    <meta name="description" content={description}>
	<html lang="de" />
</svelte:head>