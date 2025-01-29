<script lang="ts">
	import { SearchCheck, ChartArea, Siren, Link, Zap, TvMinimalPlay } from 'lucide-svelte';

	interface Feature {
		icon: any;
		title: string;
		description: string;
	}

	const features: Feature[] = [
		{
			icon: SearchCheck,
			title: 'Instant Insights',
			description:
				"Paste your smart contract address, and we'll fetch all the relevant data for you—no manual setup needed."
		},
		{
			icon: ChartArea,
			title: 'Real-Time Analytics',
			description:
				'Get detailed transaction history, performance metrics, and on-chain activity at a glance.'
		},
		{
			icon: Siren,
			title: 'Custom Alerts',
			description:
				'Stay ahead of issues with notifications for anomalies, failed transactions, and key contract events.'
		},
		{
			icon: Link,
			title: 'Expand Beyond Solana',
			description: 'Seamless future support for EVM chains, Bitcoin, and emerging blockchains.'
		},
		{
			icon: Zap,
			title: 'API & Webhooks',
			description: 'Integrate monitoring into your workflows with powerful APIs and webhooks.'
		},
		{
			icon: TvMinimalPlay,
			title: 'Intuitive Dashboard',
			description: 'Clean and modern interface designed for maximum efficiency and ease of use.'
		}
	];
</script>

<section class="bg-gradient-to-br from-blue-900 via-black to-blue-900 px-4 py-24 text-white">
	<div class="mx-auto max-w-6xl">
		<div class="mb-16 text-center">
			<h2 class="mb-4 text-4xl font-bold">Powerful Features for Smart Contract Monitoring</h2>
			<p class="text-xl text-gray-400">
				Everything you need to monitor and analyze your smart contracts
			</p>
		</div>

		<div class="grid gap-6 md:grid-cols-2 lg:grid-cols-3">
			{#each features as feature}
				<div class="rounded-2xl border border-white/10 bg-[#2A2A2A]/50 p-6 backdrop-blur-sm">
					<div class="mb-4 text-3xl">
						<svelte:component this={feature.icon} />
					</div>
					<h3 class="mb-3 text-xl font-semibold">{feature.title}</h3>
					<p class="leading-relaxed text-gray-400">{feature.description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<style>
	section {
		background-position: center;
		background-repeat: no-repeat;
		background-size: cover;
	}
</style>
