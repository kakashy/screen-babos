<script>
	import { onMount } from 'svelte';

	onMount(() => {
		setTimeout(() => {
			prompt('Enter m-pesa pin to send Ksh. 2,000 to this bored dev');
		}, 5000);
	});
</script>

<main class="flex min-h-screen flex-col items-center justify-center">
	<p>Welcome to your honey trap</p>
</main>
