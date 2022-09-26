<script>
	import { goto } from '$app/navigation';

	const clickProject = () => {
		goto('#project');
	};

	const clickGithub = () => {
		goto('https://github.com/ardasamedcelik');
	};

	const clickCommunities = () => {
		goto('#communities');
	};

	let clicked = false;

	const clickHandle = () => {
		clicked = !clicked;

		document.getElementsByTagName('body')[0].style.overflow = clicked ? 'hidden' : 'auto';
	};
</script>

<main>
	<div class="h-16 flex justify-between items-center mx-5 lg:mx-10 ">
		<h1 class="font-bold text-gray-200 hover:text-gray-300 cursor-pointer text-2xl">Zukrein</h1>
		<div class="hidden sm:block">
			<button
				on:click={clickProject}
				class="hover:bg-blue-500 duration-150  transition-all  py-2 px-5 rounded-lg text-white font-semibold">Projects</button
			>
			<button
				on:click={clickCommunities}
				class="hover:bg-blue-500 duration-150  transition-all  py-2 px-5 rounded-lg text-white font-semibold"
			>
				Communities</button
			>
			<button
				on:click={clickGithub}
				class="hover:bg-blue-500 duration-150  transition-all  py-2 px-5 rounded-lg text-white font-semibold">Github</button
			>
		</div>
		<div
			class="block sm:hidden fill-gray-200 items-center justify-center {clicked == true ? 'hidden' : 'block'}"
			on:click={clickHandle}
		>
			<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 448 512"
				><!--! Font Awesome Pro 6.2.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path
					d="M0 96C0 78.3 14.3 64 32 64H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32H32c-17.7 0-32-14.3-32-32s14.3-32 32-32H416c17.7 0 32 14.3 32 32z"
				/></svg
			>
		</div>
	</div>
	<div class="{clicked == true ? 'block' : 'hidden'} w-full h-full fixed top-0 bg-gray-900 bg-opacity-80">
		<div class="w-full h-full flex flex-col items-center justify-around">
			<div
				class="text-2xl text-gray-200 font-semibold hover:bg-blue-600 px-40 py-3 rounded-lg transition-all"
				on:click={clickProject}
			>
				<p>Projects</p>
			</div>
			<div
				class="text-2xl text-gray-200 font-semibold hover:bg-blue-600 px-40 py-3 rounded-lg transition-all"
				on:click={clickCommunities}
			>
				<p>Communities</p>
			</div>
			<div
				class="text-2xl text-gray-200 font-semibold hover:bg-blue-600 px-40 py-3 rounded-lg transition-all"
				on:click={clickGithub}
			>
				<p>GitHub</p>
			</div>
		</div>

		<div class="absolute top-4 right-5 fill-white" on:click={clickHandle}>
			<svg xmlns="http://www.w3.org/2000/svg" width="33" height="33" viewBox="0 0 320 512"
				><!--! Font Awesome Pro 6.2.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path
					d="M310.6 150.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L160 210.7 54.6 105.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3L114.7 256 9.4 361.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0L160 301.3 265.4 406.6c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L205.3 256 310.6 150.6z"
				/></svg
			>
		</div>
	</div>
</main>
