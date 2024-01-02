<script>
	import { onMount } from 'svelte';
	import { browser } from '$app/environment';
	import BackToTop from '$lib/components/BackToTop.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import Navbar from '$lib/components/Navbar.svelte';
	import '../app.scss';

	onMount(async () => {
		if (!browser) return;

		await import('bootstrap');
	});
</script>

<svelte:head>
	<title>Gabutz</title>
</svelte:head>

<!-- Start Navbar -->
<Navbar />
<!-- End Navbar -->

<!-- Start Main -->
<main class="flex-shrink-0">
	<slot />
</main>
<!-- End Main -->

<!-- Start Back To Top -->
<BackToTop />
<!-- End Back To Top -->

<!-- Start Footer -->
<Footer />
<!-- End Footer -->
