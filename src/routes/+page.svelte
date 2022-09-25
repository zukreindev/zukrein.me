<script>
	import About from '$lib/components/About.svelte';
	import Project from '$lib/components/Project.svelte';
	import GithubRepo from '$lib/components/GithubRepo.svelte';
	import Navbar from '$lib/components/Navbar.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import Communities from '$lib/components/Communities.svelte';
	import GoHome from '$lib/components/GoHome.svelte';

</script>

<main class="bg-gradient-to-r from-[#1a1d29] to-[#191c24]">
	<Navbar />
	<About />
	<Project />
	<Communities />
	<Footer />
	<GoHome />
</main>
