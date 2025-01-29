<script lang="ts">
	import { Check, Zap, Building2, Globe } from 'lucide-svelte';

	interface Feature {
		icon: typeof Check;
		title: string;
		description: string;
	}

	const features: Feature[] = [
		{
			icon: Check,
			title: 'Zero Setup Required',
			description:
				'Start monitoring your smart contracts instantly with just a contract address. No complex configuration needed.'
		},
		{
			icon: Zap,
			title: 'Reliable, Real-Time Monitoring',
			description:
				"Get instant notifications and real-time insights about your smart contract's performance and activities."
		},
		{
			icon: Building2,
			title: 'Built for Developers & Enterprises',
			description:
				'Powerful features and integrations that scale with your needs, from individual developers to large organizations.'
		},
		{
			icon: Globe,
			title: 'Future-Ready Cross-Chain Support',
			description:
				'Prepared for the multi-chain future with expanding support for EVM chains, Bitcoin, and emerging blockchains.'
		}
	];
</script>

<section class="px-4 py-16">
	<div class="mx-auto max-w-6xl">
		<div class="mb-16 text-center">
			<h2 class="mb-4 text-4xl font-bold">Why Choose UmaRell?</h2>
			<p class="text-xl text-gray-600">Built by developers, for developers</p>
		</div>

		<div class="mb-16 grid gap-12 md:grid-cols-2">
			{#each features as feature}
				<div class="flex gap-4">
					<div class="flex-shrink-0">
						<div
							class="flex h-12 w-12 items-center justify-center rounded-xl bg-[#0066FF] text-white"
						>
							<svelte:component this={feature.icon} size={24} />
						</div>
					</div>
					<div>
						<h3 class="mb-2 text-xl font-semibold">{feature.title}</h3>
						<p class="leading-relaxed text-gray-600">{feature.description}</p>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<style>
	section {
		background-position: center;
		background-repeat: no-repeat;
		background-size: contain;
	}
</style>
