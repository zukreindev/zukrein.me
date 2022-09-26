<script>
	import veiversa from '$lib/media/veiversa.png';
	
	let projects = [
		{
			name: 'VeivBotlist',
			photo: veiversa,
			description: 'VeivBotlist is a website that helps you to find the best bot for your server.',
			link: 'https://zukrein-me.vercel.app'
		},
		{
			name: 'Vapp',
			photo: veiversa,
			description: 'real-time messaging platform',
			link: 'https://zukrein-me.vercel.app'
		},
		{
			name: 'EraxDB',
			photo: veiversa,
			description: 'Nodejs database handler (oç emirhan kodladı)',
			link: 'https://zukrein-me.vercel.app'
		},
		{
			name: 'ZuksPost',
			photo: veiversa,
			description: 'funny video app',
			link: 'https://zukrein-me.vercel.app'
		},
		{
			name: 'ZuksPost',
			photo: veiversa,
			description: 'funny video app',
			link: 'https://zukrein-me.vercel.app'
		},
		{
			name: 'ZuksPost',
			photo: veiversa,
			description: 'funny video app',
			link: 'https://zukrein-me.vercel.app'
		},
	];
</script>

<main class="container py-8 mb-52" id="project">
	<h2 class="text-gray-200 text-4xl font-semibold">My Projects</h2>
	<div class="space-x-10 py-10 flex overflow-x-scroll">
		{#each projects as project}
			<div
				class="w-[250px] mx-auto rounded-lg shrink-0 grow-0 transition-all bg-[#242946ef] bg-cover bg-center shadow-md hover:shadow-lg"
				style="background-image: url({project.photo});"
			>
				<div class="px-3 py-4 m-3 rounded-lg bg-[#242b51d5] flex flex-col justify-between">
					<div>
						<a href="#a">
							<h5 class="mb-2 text-2xl font-bold tracking-tight  text-white">{project.name}</h5>
						</a>
						<p class="mb-3 h-11 font-normal text-gray-400">{project.description}</p>
	
					</div>
					<a
						href="#w"
						class="inline-flex items-center py-2 mr-auto px-3 text-sm font-medium text-center text-white rounded-lg focus:ring-4 focus:outline-none  bg-blue-600 hover:bg-blue-700 focus:ring-blue-800 transition-all"
					>
						Read more
						<svg
							aria-hidden="true"
							class="ml-2 -mr-1 w-4 h-4"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z"
								clip-rule="evenodd"
							/></svg
						>
					</a>
				</div>
			</div>
		{/each}
	</div>
</main>
