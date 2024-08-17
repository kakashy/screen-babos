<script>
	import Input from '$lib/components/ui/input/input.svelte';
	import Label from '$lib/components/ui/label/label.svelte';
	import ChevronLeft from 'lucide-svelte/icons/chevron-left';
	import * as HoverCard from '$lib/components/ui/hover-card';
	import Button from '$lib/components/ui/button/button.svelte';
	import { fly } from 'svelte/transition';
	import { goto } from '$app/navigation';
</script>

<svelte:head>
	<title>Sign In - Screen Babos</title>
	<meta
		name="description"
		content="Sign in to Screen Babos for a chance to win a limited slot of time on our shared server."
	/>
</svelte:head>

<main class="relative flex min-h-screen flex-col">
	<div class="blob-c">
		<div class="shape-blob one"></div>
		<div class="shape-blob two"></div>
	</div>
	<span class="mt-9 flex w-full items-center justify-between p-6"
		><a href="/"><ChevronLeft /></a>
		<p in:fly={{ y: 10, duration: 300 }} class="mx-auto">Login</p></span
	>
	<article class="mx-auto mt-1 flex max-w-3xl flex-col gap-5 p-6">
		<h1 in:fly={{ y: 20, duration: 500 }} class="font-['Space_Grotesk'] text-2xl font-bold">
			Welcome Back!
		</h1>
		<p class="text-lg">Please enter your phone number and password to continue</p>
		<form on:submit|preventDefault={() => goto('/')} action="" class="grid gap-3">
			<Label for="phone-number" class="text-lg opacity-70">Phone Number</Label>
			<Input id="phone-number" placeholder="+254701234567" type="tel" />
			<Label for="pass" class="text-lg opacity-70">Password</Label>
			<Input id="pass" placeholder="****" type="password" />
			<span class="ml-auto">
				<HoverCard.Root>
					<HoverCard.Trigger><p class="text-lime-700">Forgot password?</p></HoverCard.Trigger>
					<HoverCard.Content>Wah, sa utado?</HoverCard.Content>
				</HoverCard.Root>
			</span>
			<Button type="submit" class="p-7">Login</Button>
		</form>
	</article>
	<footer class="absolute bottom-9 flex w-full justify-center">
		<span class="flex items-center gap-2">
			<p>Don't have an account?</p>
			<a href="/signup" class="text-green-600">Sign Up</a>
		</span>
	</footer>
</main>

<style>
	.blob-c {
		min-height: 100vh;
		overflow: hidden;
		position: absolute;
		width: 100%;
		filter: blur(0px);
		z-index: -1;
	}

	.shape-blob {
		background: #e0ffdd;
		height: 300px;
		width: 300px;
		left: 400px;
		top: 0px;
		border-radius: 100%;
		transform: rotate(-180deg);
		position: absolute;
		animation:
			transform 8s ease-in-out infinite both alternate,
			movement_two 20s ease-in-out infinite both;
	}
	.shape-blob.one {
		background: #e0ffdd;
		height: 80vh;
		width: 80vh;
		top: 55vh;
		left: -10vw;
		border-radius: 100%;
		transform: rotate(-180deg);
		animation:
			transform 8s ease-in-out infinite both alternate,
			movement_two 20s ease-in-out infinite both;
	}
	.two {
		background: #e0ffdd;
		height: 60vh;
		width: 60vh;
		left: -20vh;
		top: 20vh;
		border-radius: 100%;
		transform: rotate(-180deg);
		animation:
			transform 8s ease-in-out infinite both alternate,
			movement_two 20s ease-in-out infinite both;
	}
</style>
