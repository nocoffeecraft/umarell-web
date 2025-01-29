<script lang="ts">
	import { Origami } from 'lucide-svelte';

	let showModal = false;
	let showConfirmation = false;
	let name = '';
	let email = '';
	let company = '';

	function handleSubmit() {
		showModal = false;
		showConfirmation = true;
	}
</script>

<div class="min-h-screen bg-gradient-to-br from-blue-100 via-white to-blue-200">
	<!-- Navigation -->
	<nav class="container mx-auto flex items-center justify-center px-4 py-6">
		<a href="/" class="flex items-center gap-2">
			<Origami class="h-8 w-8 text-[#4B6BFB]" />
			<span class="text-2xl font-semibold">UmaRell</span>
		</a>
	</nav>

	<!-- Hero Section -->
	<main class="container mx-auto px-4 pt-20">
		<div class="mx-auto mb-16 max-w-3xl text-center">
			<h1 class="mb-6 text-6xl font-bold leading-tight text-black md:text-7xl">
				No Setup. No Stress.
			</h1>
			<p class="mb-8 text-lg leading-relaxed text-gray-600 md:text-xl">
				Drop your smart contract address, and we’ll handle the rest. Track transactions, detect
				anomalies, and get notified in real time—without the complexity.
			</p>
			<button
				on:click={() => (showModal = true)}
				class="inline-flex rounded-full bg-black px-6 py-3 font-medium text-white transition-colors hover:bg-gray-700"
			>
				Get started for free
			</button>
		</div>
		<div class="relative flex h-[500px] items-start justify-center overflow-hidden">
			<img
				src="src/lib/assets/dashboard.jpg"
				alt="dashboard"
				class="w-5/6 rounded-2xl border-8 border-blue-200 object-cover shadow-2xl"
			/>
		</div>
	</main>
</div>

{#if showModal}
	<div class="fixed inset-0 flex items-center justify-center bg-black bg-opacity-50">
		<div class="w-1/3 rounded-lg bg-white p-8 shadow-lg">
			<h2 class="mb-4 text-2xl font-bold">Get Started for Free</h2>
			<form on:submit|preventDefault={handleSubmit}>
				<div class="mb-4">
					<label for="name" class="mb-2 block text-sm font-medium text-gray-900">Your Name</label>
					<input
						id="name"
						type="text"
						bind:value={name}
						class="w-full rounded border p-2"
						required
					/>
				</div>
				<div class="mb-4">
					<label for="email" class="mb-2 block text-sm font-medium text-gray-900">Your Email</label>
					<input
						id="email"
						type="email"
						bind:value={email}
						class="w-full rounded border p-2"
						required
					/>
				</div>
				<div class="mb-4">
					<label for="company" class="mb-2 block text-sm font-medium text-gray-900"
						>Your Comapny Name</label
					>
					<input
						id="company"
						type="text"
						bind:value={company}
						class="w-full rounded border p-2"
						required
					/>
				</div>

				<div class="flex justify-end gap-4">
					<button
						type="button"
						on:click={() => (showModal = false)}
						class="rounded bg-gray-300 px-4 py-2">Close</button
					>
					<button type="submit" class="rounded bg-blue-500 px-4 py-2 text-white">Submit</button>
				</div>
			</form>
		</div>
	</div>
{/if}

{#if showConfirmation}
	<div class="fixed inset-0 flex items-center justify-center bg-black bg-opacity-50">
		<div class="rounded-lg bg-white p-8 shadow-lg">
			<h2 class="mb-4 text-2xl font-bold">Thank You!</h2>
			<p class="mb-4">Your submission has been received. We will get back to you shortly.</p>
			<div class="flex justify-end gap-4">
				<button on:click={() => (showConfirmation = false)} class="rounded bg-gray-300 px-4 py-2"
					>Close</button
				>
				<button
					on:click={() => (showConfirmation = false)}
					class="rounded bg-blue-500 px-4 py-2 text-white">OK</button
				>
			</div>
		</div>
	</div>
{/if}

<style>
	:global(html) {
		background-image: url('https://hebbkx1anhila5yf.public.blob.vercel-storage.com/image-RvasExfylUtKRrkhATNMfnriJ0gUjE.png');
		background-size: cover;
		background-position: center;
		background-repeat: no-repeat;
	}
</style>
