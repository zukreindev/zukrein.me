<script>
	let projects = [
		{
			name: 'VeivBotlist',
			photo: 'https://img.myloview.com/stickers/z-logo-design-icon-vector-symbol-700-194355775.jpg',
			description: 'VeivBotlist is a website that helps you to find the best bot for your server.',
			link: 'https://zukrein-me.vercel.app'
		},
		{
			name: 'Vapp',
			photo: 'https://img.myloview.com/stickers/z-logo-design-icon-vector-symbol-700-194355775.jpg',
			description: 'real-time messaging platform',
			link: 'https://zukrein-me.vercel.app'
		},
		{
			name: 'EraxDB',
			photo: 'https://img.myloview.com/stickers/z-logo-design-icon-vector-symbol-700-194355775.jpg',
			description: 'Nodejs database handler (oç emirhan kodladı)',
			link: 'https://zukrein-me.vercel.app'
		},
		{
			name: 'ZuksPost',
			photo: 'https://img.myloview.com/stickers/z-logo-design-icon-vector-symbol-700-194355775.jpg',
			description: 'funny video app',
			link: 'https://zukrein-me.vercel.app'
		},
		{
			name: 'Voxe',
			photo: 'https://img.myloview.com/stickers/z-logo-design-icon-vector-symbol-700-194355775.jpg',
			description: 'RPG bot',
			link: 'https://zukrein-me.vercel.app'
		}
	];
</script>

<main class="ml-12">
	<h2 class="text-gray-200 text-4xl ml-10 font-semibold">My Projects</h2>
	<div class="mt-10 grid gap-10 grid-cols-3 ml-3 w-full mx-auto">
		{#each projects as project}
			<div class="w-[300px]   rounded-lg border   transition-all bg-[#242946ef] border-gray-800 shadow-md hover:shadow-lg">
				<a href="#c">
					<img class="rounded-t-lg w-full" src={project.photo} alt="" />
				</a>
				<div class="p-5">
					<a href="#a">
						<h5 class="mb-2 text-2xl font-bold tracking-tight  text-white">{project.name}</h5>
					</a>
					<p class="mb-3 font-normal text-gray-400">{project.description}</p>

					<a
						href="#w"
						class="inline-flex items-center py-2 px-3 text-sm font-medium text-center text-white  rounded-lg  focus:ring-4 focus:outline-none  bg-blue-600 hover:bg-blue-700 focus:ring-blue-800"
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
