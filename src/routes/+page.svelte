<script>
	import Sidebar from '$lib/components/Sidebar.svelte';
	import About from '$lib/components/About.svelte';
	import Project from '$lib/components/Project.svelte';
	import Social from '$lib/components/Social.svelte';
		let selectednum = 2;

	/**
	 * @type {number}
	 */
	let y_eksen;
	let tag = 'div';
</script>

<main class="flex h-[9050px]">
	<!--Sidebar-->
	<div>
		{#if y_eksen > 500}
			<Sidebar selected={2} />
		{:else if y_eksen > 200}
			<Sidebar selected={3} />
		{:else}
			<Sidebar selected={1} />
		{/if}
	</div>
	<!--Main Content-->
	<div class=" py-3">
		<About />
		<Project />
		<Social />
		
	</div>
</main>

<svelte:window bind:scrollY={y_eksen} />
