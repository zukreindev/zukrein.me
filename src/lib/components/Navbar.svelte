<script>
// @ts-nocheck

    import {goto} from "$app/navigation"
    const clickProject = () => {
        goto("#project")
    }
    const clickGithub = () => {
        goto("#github")
    }
    const clickCommunities = () => {
        goto("#communities")
    }
    
	
</script>

<main class="h-14 flex justify-between  items-center mx-5 lg:mx-10 ">
	<h1 class="font-bold text-gray-200 hover:text-gray-300 cursor-pointer text-2xl">Zukrein</h1>
	<div>
		<button on:click={clickProject} class="hover:bg-blue-500 duration-150  transition-all  py-2 px-5 rounded-lg text-white font-semibold"
			>Projects</button
		>
		<button on:click={clickCommunities}  class="hover:bg-blue-500 duration-150  transition-all  py-2 px-5 rounded-lg text-white font-semibold">
			Communities</button
		>
		<button on:click={clickGithub} class="hover:bg-blue-500 duration-150  transition-all  py-2 px-5 rounded-lg text-white font-semibold"
			>Github</button
		>
	</div>
</main>
