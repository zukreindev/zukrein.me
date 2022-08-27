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

				if (discordstatus == 'online') {
					discordpresence = '📱 Online';
				} else if (discordstatus == 'idle') {
					discordpresence = '🌙 Idle';
				} else if (discordstatus == 'dnd') {
					discordpresence = '🔴 Do Not Disturb';
				} else if (discordstatus == 'offline') {
					discordpresence = 'ring-gray-500';
				}
			});
		});
	});
</script>

<main class="">
	<div class="md:flex px-auto md:mx-36 py-20 md:py-56 text-white items-center justify-between">
		<div class="">
			<img src={discordpp} class="w-52 rounded-full ring-4  {discordstatus === 'dnd' ? 'ring-red-500' : ''} {discordstatus === 'offline' ? 'ring-gray-500' : ''} {discordstatus === 'online' ? 'ring-green-500' : ''} {discordstatus === 'idle' ? 'ring-yellow-500' : ''}"  alt=""/>
		</div>
		<div class="text-xl pt-7 flex-row text-center md:text-left md:pl-6 mx-6">
			<h3 class="text-2xl font-medium pb-4 md:pb-3 text-white ">Hello World 😺</h3>
			<p class="text-gray-200 font-medium ">
				Hello, I'm Zukrein! I'm 16 years old, I'm a full-stack developer. I living in Turkey
			</p>
		</div>
	</div>
</main>
