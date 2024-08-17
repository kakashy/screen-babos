<script>
	import Button from '$lib/components/ui/button/button.svelte';
	import { fly } from 'svelte/transition';
</script>

<main
	in:fly={{ y: 10, duration: 300 }}
	class="flex min-h-screen flex-col items-center justify-center p-5"
>
	<div class="mx-auto grid place-items-center gap-5 rounded bg-muted p-5 shadow">
		<h1 class="text-xl font-semibold">Something went wrong</h1>
		<a href="/">
			<Button>Go back home</Button>
		</a>
	</div>
</main>
