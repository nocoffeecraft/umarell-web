<script>
	import '../app.css';
</script>

<div class="min-h-screen bg-white font-sans text-gray-900">
	<main>
		<slot />
	</main>

	<footer class="mt-20 bg-gray-100 py-8"></footer>
</div>

<style>
	:global(html) {
		scroll-behavior: smooth;
	}
</style>
