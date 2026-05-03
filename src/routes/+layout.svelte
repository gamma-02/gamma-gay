<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
    <link rel="icon" href={favicon} />
    <link rel="stylesheet" href="/smui-dark.css" media="(prefers-color-scheme: light)" />
    <link
            rel="stylesheet"
            href="/smui-dark.css"
            media="screen and (prefers-color-scheme: dark)"
    />
</svelte:head>
{@render children()}
