<script>
	import Hero from '$lib/components/Hero.svelte';
	import Features from '$lib/components/Features.svelte';
	import HowItWorks from '$lib/components/HowItWorks.svelte';
	import WhyChoose from '$lib/components/WhyChoose.svelte';
	import FinalCTA from '$lib/components/FinalCTA.svelte';
</script>

<svelte:head>
	<title>UmaRell - Smart Contract Monitoring for Solana</title>
</svelte:head>

<Hero />
<Features />
<div class="bg-gradient-to-br from-blue-100 via-white to-blue-200">
	<HowItWorks />
	<WhyChoose />
</div>
<FinalCTA />
