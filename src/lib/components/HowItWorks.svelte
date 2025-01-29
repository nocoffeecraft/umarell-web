<script lang="ts">
	const steps = [
		{
			number: 1,
			title: 'Enter your contract address',
			description:
				'No configuration required. Simply paste your Solana smart contract address to get started.',
			content: `<div class="bg-gray-50 rounded-lg p-4 mt-4">
        <input 
          type="text" 
          placeholder="solana.contract.address..." 
          class="w-full p-3 rounded-md border border-gray-200 bg-white text-gray-600 font-mono text-sm"
        />
      </div>`
		},
		{
			number: 2,
			title: 'View real-time analytics',
			description:
				'Access comprehensive dashboard showing transactions, events, and contract health in one place.',
			content: `<div class="bg-[#0066FF]/10 rounded-lg p-4 mt-4">
        <div class="h-2 rounded-full bg-[#6B8BF5]/20">
          <div class="h-full w-3/4 rounded-full bg-[#0066FF]"></div>
        </div>
      </div>`
		},
		{
			number: 3,
			title: 'Set up alerts',
			description: 'Get notified about anomalies, errors, or custom triggers instantly.',
			content: `<div class="mt-4">
        <span class="inline-flex items-center px-3 py-1 rounded-full text-sm bg-green-100 text-green-700">
          Alerts Active
        </span>
      </div>`
		}
	];
</script>

<section class="px-4 py-16">
	<div class="mx-auto max-w-6xl">
		<div class="mb-16 text-center">
			<h2 class="mb-4 text-4xl font-bold">How It Works</h2>
			<p class="text-xl text-gray-600">
				Start monitoring your smart contracts in three simple steps
			</p>
		</div>

		<div class="grid gap-8 md:grid-cols-3">
			{#each steps as step}
				<div class="relative">
					<div class="absolute -left-3 top-0">
						<div
							class="flex h-12 w-12 items-center justify-center rounded-full bg-[#0066FF] text-lg font-semibold text-white"
						>
							{step.number}
						</div>
					</div>
					<div class="pl-14">
						<h3 class="mb-3 text-xl font-semibold">{step.title}</h3>
						<p class="mb-4 text-gray-600">{step.description}</p>
						{@html step.content}
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
