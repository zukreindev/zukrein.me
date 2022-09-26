<script>
	import { onMount } from 'svelte';

	/**
	 * @type {string}
	 */
	let discord_pp;

	/**
	 * @type {string}
	 */
	let discord_status;

	onMount(async () => {
		fetch('https://api.lanyard.rest/v1/users/888795101843820564').then((e) => {
			e.json().then((e) => {
				discord_pp = e.data.discord_user.avatar;
				discord_status = e.data.discord_status;
				discord_pp = discord_pp
					? `https://cdn.discordapp.com/avatars/888795101843820564/${discord_pp}.${discord_pp.startsWith('a_') ? 'gif' : 'png'}`
					: 'https://cdn.discordapp.com/embed/avatars/1.png';
			});
		});
	});
</script>

<main class="">
	<div class="lg:flex items-center lg:py-52 lg:px-64 w-full justify-evenly ">
		<div class="">
			<img
				src={discord_pp}
				class="lg:w-72 md:w-60 w-52  mx-auto rounded-full ring-2  {discord_status === 'dnd'
					? 'ring-red-500'
					: ''} {discord_status === 'offline' ? 'ring-gray-500' : ''} {discord_status === 'online'
					? 'ring-green-500'
					: ''} {discord_status === 'idle' ? 'ring-yellow-500' : ''}"
				alt=""
			/>
		</div>
		<div class="flex flex-col items-center justify-center">
			<h3 class="text-4xl font-medium pb-4 w-64 lg:pb-3 text-gray-50 ">Hello World 😺</h3>
			<p class="text-gray-400 text-lg font-medium w-64 items-center">
				Hello, I'm Zukrein! I'm 16 years old, I'm a full-stack developer. I living in Turkey
			</p>
		</div>
	</div>
</main>
