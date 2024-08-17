<script>
	import Button from '$lib/components/ui/button/button.svelte';
	import { fade, fly, scale } from 'svelte/transition';
</script>

<svelte:head>
	<title>Screen Babos</title>
	<meta name="description" content="Crypto payments made easy." />
</svelte:head>

<main class="relative flex min-h-screen flex-col gap-3">
	<div class="blob-c">
		<div class="shape-blob lite tuta"></div>
		<div class="shape-blob lite mosi"></div>
		<div class="shape-blob lite mbwegze"></div>
		<div class="shape-blob one"></div>
		<div class="shape-blob two"></div>
	</div>
    <img in:scale={{ duration: 500}} src="https://images.unsplash.com/photo-1542321888-8a6abb3ec824?q=80&w=870&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="Man holding a phone" class='rounded-full object-cover w-28 h-28 absolute left-2/3 top-[10vh] md:w-60 md:h-60 lg:w-80 lg:h-80'>
    <img in:scale={{ duration: 500}} src="/img/lisa-marie-theck-PF6JfGfmqOI-unsplash.jpg" alt="a woman sitting on a couch looking at her cell phone. This is by Lisa Marie Theck on Unsplash" class='rounded-full object-cover w-44 h-44 absolute left-1/3 top-[25vh] md:w-60 md:h-60 lg:w-80 lg:h-80'>
	<article class="mt-auto p-5 flex flex-col gap-3 max-w-2xl mx-auto">
		<h1 in:fly={{ y: 20, duration: 500 }} class="w-2/3 font-['Space_Grotesk'] text-2xl font-bold">Crypto Payments made Easy</h1>
		<p in:fade={{ duration: 400, delay: 200 }} class="text-lg">Make payments for your day to day purchases directly from your wallet</p>
		<a href="/signin" class="my-10">
            <Button class="w-full">Get Started</Button>
        </a>
	</article>
</main>

<style>
	.blob-c {
		min-height: 100vh;
		overflow: hidden;
		position: absolute;
		width: 100%;
		filter: blur( 0px);
		z-index: -1;
		/*   background: rgba(255,255,255,0.1) */
	}

	.shape-blob {
		background: #062331;
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
		background: #062331;
		height: 60vh;
		width: 60vh;
		top: 1vh;
        left: 60vw;
		border-radius: 100%;
		transform: rotate(-180deg);
		animation:
			transform 8s ease-in-out infinite both alternate,
			movement_two 20s ease-in-out infinite both;
	}
	.two {
		background: #062331;
		height: 60vh;
		width: 60vh;
		left: 10px;
		top: -300px;
		border-radius: 100%;
		transform: rotate(-180deg);
		animation:
			transform 8s ease-in-out infinite both alternate,
			movement_two 20s ease-in-out infinite both;
	}
    .lite {
        z-index: 1;
        background-color: #ffffff20;
        width: 80px;
        height:80px;
        animation: movement_one 20s ease-in-out infinite both;
    }
    .mosi {
        top: -40px;
        left: 30vw;
        width: 80px;
        height: 80px;
    }
    .mbwegze {
        top: 25vh;
        left: 50vw;
        width: 30px;        
        height: 30px;        
    }
    .tuta {
        top: 5vh;
        left: 70vw;
        width: 50px;        
        height: 50px;        
    }

	@keyframes transform {
		/* 0%,
		100% {
			border-radius: 99% 95% 100% 94% / 91% 92% 99% 100%;
		}
		20% {
			border-radius: 98% 96% 99% 91% / 93% 94% 98% 99%;
		}
		40% {
			border-radius: 88% 89% 95% 99% / 95% 96% 96% 98%;
		}
		60% {
			border-radius: 90% 90% 97% 95% / 96% 98% 99% 100%;
		}
		80% {
			border-radius: 88% 89% 95% 99% / 95% 96% 96% 98%;
		} */
	}

	@keyframes movement_one {
		0%,
		100% {
			transform: none;
		}
		50% {
			transform: translate(50%, 20%) rotateY(10deg) scale(1);
		}
	}

	@keyframes movement_two {
		0%,
		500% {
			transform: none;
		}
		50% {
			transform: translate(5%, 2%) rotate(-200deg) scale(1.3);
		}
	}
</style>
