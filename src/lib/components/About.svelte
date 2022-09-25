<script>
	/**
	 * @type {string}
	 */
	let discordpp;
	let discordppcode;
	/**
	 * @type {string}
	 */
	let discordpresence;
	/**
* @type {string}
*/
	let discordstatus;
	/**
	 * @type {string}
	 */
	let dicordid;
	import { onMount } from 'svelte';

	onMount(async () => {
		fetch('https://api.lanyard.rest/v1/users/888795101843820564').then((e) => {
			e.json().then((e) => {
				dicordid = e.data.discord_user.id;
				discordpp = e.data.discord_user.avatar;
				discordstatus = e.data.discord_status;
				discordpp = discordpp
					? `https://cdn.discordapp.com/avatars/888795101843820564/${discordpp}.${discordpp.startsWith('a_') ? 'gif' : 'png'}`
					: 'https://cdn.discordapp.com/embed/avatars/1.png';

				
			});
		});
	});
</script>

<main class="">
	<div class="lg:flex items-center lg:py-52 lg:px-64 w-full justify-evenly ">
		<div class="">
			<img src={discordpp} class="lg:w-72 md:w-60 w-52  mx-auto rounded-full ring-2  {discordstatus === 'dnd' ? 'ring-red-500' : ''} {discordstatus === 'offline' ? 'ring-gray-500' : ''} {discordstatus === 'online' ? 'ring-green-500' : ''} {discordstatus === 'idle' ? 'ring-yellow-500' : ''}"  alt=""/>
		</div>
		<div class="flex flex-col items-center justify-center">
			<h3 class="text-4xl font-medium pb-4 w-64 lg:pb-3 text-gray-50 ">Hello World 😺</h3>
			<p class="text-gray-400 text-lg font-medium w-64 items-center">
				Hello, I'm Zukrein! I'm 16 years old, I'm a full-stack developer. I living in Turkey
			</p>
		</div>
	</div>
</main>
