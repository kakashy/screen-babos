<script>
	import Button from "$lib/components/ui/button/button.svelte";
	import { fly } from "svelte/transition";

</script>
<main in:fly={{ y: 10, duration: 300}} class="min-h-screen flex flex-col items-center justify-center p-5">
    <div class="rounded p-5 shadow mx-auto bg-muted grid place-items-center gap-5">
        <h1 class="text-xl font-semibold">Something went wrong</h1>
        <a href="/">
        <Button>Go back home</Button>
        </a>
    </div>
</main>