<script>
	import welcome_fallback from '$lib/images/svelte-welcome.png';
	import welcome from '$lib/images/svelte-welcome.webp';
	import { Button } from '$lib/shadcn/ui/button';
	import { Alert } from 'flowbite-svelte';
	import Counter from './Counter.svelte';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<h1>
		<Alert>
			<span class="font-medium">Default alert!</span>
			Change a few things up and try submitting again.
		</Alert>
		<Alert color="blue">
			<span class="font-medium">Info alert!</span>
			Change a few things up and try submitting again.
		</Alert>
		<Alert color="red">
			<span class="font-medium">Danger alert!</span>
			Change a few things up and try submitting again.
		</Alert>
		<Alert color="green">
			<span class="font-medium">Success alert!</span>
			Change a few things up and try submitting again.
		</Alert>
		<Alert color="yellow">
			<span class="font-medium">Warning alert!</span>
			Change a few things up and try submitting again.
		</Alert>
		<Alert color="dark">
			<span class="font-medium">Dark alert!</span>
			Change a few things up and try submitting again.
		</Alert>

		<Button>Click me</Button>
		<span class="welcome">
			<picture>
				<source srcset={welcome} type="image/webp" />
				<img src={welcome_fallback} alt="Welcome" />
			</picture>
		</span>

		to your new<br />SvelteKit app
	</h1>

	<h2>
		try editing <strong>src/routes/+page.svelte</strong>
	</h2>

	<Counter />
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
</style>
