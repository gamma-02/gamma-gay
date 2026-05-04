<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/Gamma_uc_lc.svg';
    // import styles from '$lib/assets/styles.css'

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
<!--    <link rel="stylesheet" href="{styles}"/>-->
</svelte:head>
{@render children()}
