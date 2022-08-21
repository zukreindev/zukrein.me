<script>
	import { onMount } from 'svelte';
	//GitHub Repositories
	/**
	 * @type {any}
	 */
	let githubrepo;
	let wyh = false;
	fetch('https://api.github.com/users/ardasamedcelik/repos').then((response) => {
		console.log(' response', response);
		console.log(' r.json() >', response.clone().json()); //
		response.json().then((json) => {
			console.log('json', json);
			githubrepo = json;
			wyh = true;
		});
	});

	//Github User Info
	/**@type {string}*/
	let username
	/**@type {string}*/
	let description;
	/**@type {string}*/
	let location;
	/**@type {string}*/
	let avatar
	/**@type {string}*/
	let followers;

	onMount(async () => {
		await fetch('https://api.github.com/users/ardasamedcelik').then((e) => {e.json().then((e) => {
			username = e.login;
			description = e.bio;
			location = e.location;
			avatar = e.avatar_url;
			followers = e.followers;

			console.log('username', username);
			console.log("deneme")
		});
	});
	});
</script>

<main>
	{#if wyh}
		{#each githubrepo as deneme}
			<div />
		{/each}
	{/if}

	<div class="mx-auto mt-32 px-4 py-4 flex  w-[900px] bg-[#0d1117af] rounded-lg shadow-lg">
		<div class="items-center">
			<img src={avatar} class="w-52 rounded-full" alt="aa">
			<p class="text-white font-bold text-2xl my-2">{username}</p>
			<p class="text-gray-300 text-[12px] py-3 px-2 w-56">{description}</p>
			<div class="my-2 mr-4 flex flex-col ">
				<button type="button" class="text-white bg-[#24292F] hover:bg-[#24292F]/90 focus:ring-4 focus:outline-none focus:ring-[#24292F]/50 font-medium rounded-lg text-sm px-5 py-2.5 text-center inline-flex items-center dark:focus:ring-gray-500 dark:hover:bg-[#050708]/30 mr-2 mb-2">
					Followers: {followers}
				  </button>
				  
				<button type="button" class="text-white bg-[#24292F] hover:bg-[#24292F]/90 focus:ring-4 focus:outline-none focus:ring-[#24292F]/50 font-medium rounded-lg text-sm px-5 py-2.5 text-center inline-flex items-center dark:focus:ring-gray-500 dark:hover:bg-[#050708]/30 mr-2 mb-2">
					Follow: {followers}
				  </button>
				  
				<button type="button" class="text-white bg-[#24292F] hover:bg-[#24292F]/90 focus:ring-4 focus:outline-none focus:ring-[#24292F]/50 font-medium rounded-lg text-sm px-5 py-2.5 text-center inline-flex items-center dark:focus:ring-gray-500 dark:hover:bg-[#050708]/30 mr-2 mb-2">
					Location: {followers}
				  </button>
			</div>
		</div>

		<div>
			<!--Company ve repolar-->
			<div>
				<h2 class="text-white font-bold text-xl py-3">Company</h2>
				<div class="flex">
					<div class="h-24 w-40 bg-gray-800 rounded-md mx-3 my-3">
						
					</div>
					<div class="h-24 w-40 bg-gray-800 rounded-md mx-3 my-3">
							
					</div>
				</div>
			</div>
		</div>
	</div>
</main>
