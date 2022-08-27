<script>
	import Sidebar from '$lib/components/Sidebar.svelte';
	import About from '$lib/components/About.svelte';
	import Project from '$lib/components/Project.svelte';
	import Social from '$lib/components/Social.svelte';
	import GithubRepo from '$lib/components/GithubRepo.svelte';
	import Navbar from '$lib/components/Navbar.svelte';

		let selectednum = 0;

	/**
	 * @type {number}
	 */
	let y_eksen;
	let tag = 'div';
</script>
<main class="flex h-[9050px]">
	
	<!--Sidebar-->
	<div>
		{#if y_eksen > 1300}
			<Sidebar selected={3} />
		{:else if y_eksen > 600}
			<Sidebar selected={2} />
		{:else}
			<Sidebar selected={1} />
		{/if}
	</div>
	<!--Main Content-->
	<div class="py-3 ml-20">
		<Navbar />
		<About />
		<Project />
		<GithubRepo />
		<Social />
		
	</div>
</main>

<svelte:window bind:scrollY={y_eksen} />
