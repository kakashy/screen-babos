<script>
	import { fade } from 'svelte/transition';
</script>

<svelte:head>
	<title>Sign Up</title>
	<meta name="description" content="Use this page to not sign up" />
</svelte:head>

<main class="flex min-h-screen flex-col items-center justify-center">
	<a href="/" in:fade={{ duration: 800 }}>
		<h1 class="text-5xl">No</h1>
	</a>
</main>
