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
	let username;
	/**@type {string}*/
	let description;
	/**@type {string}*/
	let location;
	/**@type {string}*/
	let avatar;
	/**@type {string}*/
	let followers;
	/**
	 * @type {any}
	 */
	let following;
	let why = false;
	onMount(async () => {
		await fetch('https://api.github.com/users/ardasamedcelik').then((e) => {
			e.json().then((e) => {
				username = e.login;
				description = e.bio;
				location = e.location;
				avatar = e.avatar_url;
				followers = e.followers;
				following = e.following;
				why = true;
				console.log('username', username);
				console.log('deneme');
			});
		});
	});

	import FaStar from 'svelte-icons/fa/FaStar.svelte';
	import IoMdTv from 'svelte-icons/io/IoMdTv.svelte';
</script>

<main>
	{#if why}
		<h2 class="ml-14 mt-32 text-white text-4xl font-semibold mb-3 pb-3">GitHub Profile</h2>

		<div class="px-4 py-4 mx-14 bg-[#0d1117af] rounded-lg shadow-lg">
			<div class="flex">
				<div class="items-center">
					<img src={avatar} class="w-52 rounded-full" alt="aa" />
					<p class="text-white font-bold text-2xl my-2">{username}</p>
					<p class="text-gray-300 text-[12px] py-3 px-2 w-56">{description}</p>
					<div class="my-2 mr-4 flex flex-col ">
						<button
							type="button"
							class="text-white bg-[#24292F] hover:bg-[#24292F]/90 focus:ring-4 focus:outline-none focus:ring-[#24292F]/50 font-medium rounded-lg text-sm px-5 py-2.5 text-center inline-flex items-center dark:focus:ring-gray-500 dark:hover:bg-[#050708]/30 mr-2 mb-2"
						>
							Followers: {followers}
						</button>

						<button
							type="button"
							class="text-white bg-[#24292F] hover:bg-[#24292F]/90 focus:ring-4 focus:outline-none focus:ring-[#24292F]/50 font-medium rounded-lg text-sm px-5 py-2.5 text-center inline-flex items-center dark:focus:ring-gray-500 dark:hover:bg-[#050708]/30 mr-2 mb-2"
						>
							Follow: {following}
						</button>

						<button
							type="button"
							class="text-white bg-[#24292F] hover:bg-[#24292F]/90 focus:ring-4 focus:outline-none focus:ring-[#24292F]/50 font-medium rounded-lg text-sm px-5 py-2.5 text-center inline-flex items-center dark:focus:ring-gray-500 dark:hover:bg-[#050708]/30 mr-2 mb-2"
						>
							Location: {location}
						</button>
					</div>
				</div>

				<div>
					<!--Repositories-->
					<div>
						<h2 class="text-white font-bold text-xl py-3">Repositories</h2>
						<div class="grid grid-cols-3 gap-7">
							{#if wyh}
								{#each githubrepo as repo}
									<a href={repo.html_url} target="_blank" rel="noopener noreferrer">
										<div class=" w-52 bg-gray-800 rounded-md mx-3 my-2 p-1 pl-3">
											<h3 class="text-[14px] text-white font-bold">{repo.name}</h3>

											<div class="flex items-center">
												<div class="flex items-center mr-2">
													<div class="star mr-1">
														<FaStar />
													</div>
													<h2 class="text-white text-[12px] flex my-1">{repo.watchers_count}</h2>
												</div>
												<div class="flex items-center">
													<div class="tv mr-1">
														<IoMdTv />
													</div>
													<h2 class="text-white text-[12px] flex mb-1">{repo.watchers_count}</h2>
												</div>
											</div>
											<h2 class="text-gray-300 text-[10px] font-medium">{repo.language}</h2>
										</div>
									</a>
								{/each}
							{/if}
						</div>
					</div>
				</div>
			</div>
		</div>
	{/if}
</main>

<style>
	.star {
		color: #ffc107;
		width: 12px;
		height: 12px;
	}
	.tv {
		color: #ffffff;
		width: 12px;
		height: 12px;
	}
</style>
