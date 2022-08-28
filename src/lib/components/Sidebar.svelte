<script>
	import { goto } from '$app/navigation';

	export /**
	 * @type {number}
	 */
	let selected;
</script>

<div class="hidden  h-screen w-16 bg-gradient-to-b from-[#12141d41] to-[#37427200] lg:flex flex-col fixed">
	{#if selected === 1}
		<div class="flex  justify-center mt-10 mx-auto p-3 rounded-lg bg-blue-600 hover:bg-blue-700 transition-all  cursor-pointer">
			<svg width="34" height="34" fill="none" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M10.55 2.532a2.25 2.25 0 0 1 2.9 0l6.75 5.692c.507.428.8 1.057.8 1.72v9.803a1.75 1.75 0 0 1-1.75 1.75h-3.5a1.75 1.75 0 0 1-1.75-1.75v-5.5a.25.25 0 0 0-.25-.25h-3.5a.25.25 0 0 0-.25.25v5.5a1.75 1.75 0 0 1-1.75 1.75h-3.5A1.75 1.75 0 0 1 3 19.747V9.944c0-.663.293-1.292.8-1.72l6.75-5.692Zm1.933 1.147a.75.75 0 0 0-.966 0L4.767 9.37a.75.75 0 0 0-.267.573v9.803c0 .138.112.25.25.25h3.5a.25.25 0 0 0 .25-.25v-5.5c0-.967.784-1.75 1.75-1.75h3.5c.966 0 1.75.783 1.75 1.75v5.5c0 .138.112.25.25.25h3.5a.25.25 0 0 0 .25-.25V9.944a.75.75 0 0 0-.267-.573l-6.75-5.692Z" fill="#fff"/></svg>
		</div>

		<div
			on:click={() => {
				goto('');
			}}
			class="flex  justify-center mt-2 mx-auto p-3 rounded-lg hover:bg-blue-700 transition-all cursor-pointer"
		>
			<svg width="34" height="34" fill="none" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"
				><path
					d="m8.086 18.611 5.996-14.004a1 1 0 0 1 1.878.677l-.04.11-5.996 14.004a1 1 0 0 1-1.878-.677l.04-.11 5.996-14.004L8.086 18.61Zm-5.793-7.318 4-4a1 1 0 0 1 1.497 1.32l-.083.094L4.414 12l3.293 3.293a1 1 0 0 1-1.32 1.498l-.094-.084-4-4a1 1 0 0 1-.083-1.32l.083-.094 4-4-4 4Zm14-4.001a1 1 0 0 1 1.32-.083l.093.083 4.001 4.001a1 1 0 0 1 .083 1.32l-.083.095-4.001 3.995a1 1 0 0 1-1.497-1.32l.084-.095L19.584 12l-3.293-3.294a1 1 0 0 1 0-1.414Z"
					fill="#fff"
				/></svg
			>
		</div>
		<div class="flex  justify-center mt-2 mx-auto p-3 rounded-lg hover:bg-blue-700 transition-all cursor-pointer">
			<svg width="34" height="34" fill="none" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"
				><path
					d="M6.19 21.854a.75.75 0 0 1-1.188-.61V6.25a3.25 3.25 0 0 1 3.25-3.25h7.499A3.25 3.25 0 0 1 19 6.249v14.996a.75.75 0 0 1-1.188.609l-5.811-4.181-5.812 4.18Z"
					fill="#fff"
				/></svg
			>
		</div>
	{:else if selected === 2}
		<div class="flex  justify-center mt-10 mx-auto p-3 rounded-lg  hover:bg-blue-700 transition-all cursor-pointer">
			<svg width="24" height="24" fill="none" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M10.55 2.532a2.25 2.25 0 0 1 2.9 0l6.75 5.692c.507.428.8 1.057.8 1.72v9.803a1.75 1.75 0 0 1-1.75 1.75h-3.5a1.75 1.75 0 0 1-1.75-1.75v-5.5a.25.25 0 0 0-.25-.25h-3.5a.25.25 0 0 0-.25.25v5.5a1.75 1.75 0 0 1-1.75 1.75h-3.5A1.75 1.75 0 0 1 3 19.747V9.944c0-.663.293-1.292.8-1.72l6.75-5.692Zm1.933 1.147a.75.75 0 0 0-.966 0L4.767 9.37a.75.75 0 0 0-.267.573v9.803c0 .138.112.25.25.25h3.5a.25.25 0 0 0 .25-.25v-5.5c0-.967.784-1.75 1.75-1.75h3.5c.966 0 1.75.783 1.75 1.75v5.5c0 .138.112.25.25.25h3.5a.25.25 0 0 0 .25-.25V9.944a.75.75 0 0 0-.267-.573l-6.75-5.692Z" fill="#fff"/></svg>
		</div>

		<div
			on:click={() => {
				goto('');
			}}
			class="flex  justify-center mt-2 mx-auto p-3 rounded-lg bg-blue-600 hover:bg-blue-700 transition-all cursor-pointer"
		>
		<svg width="24" height="24" fill="none" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="m10.542 8.608 1.1-2.23a.678.678 0 0 1 1.216 0l1.1 2.23 2.461.357c.556.08.778.764.376 1.157l-1.78 1.735.42 2.45a.678.678 0 0 1-.984.716l-2.201-1.157-2.2 1.157a.678.678 0 0 1-.985-.715l.42-2.45-1.78-1.736a.678.678 0 0 1 .376-1.157l2.46-.357Zm1.058.92a.678.678 0 0 1-.51.37l-1.454.212 1.052 1.025c.16.156.232.38.195.6l-.249 1.448 1.3-.684a.678.678 0 0 1 .632 0l1.3.684-.249-1.448a.678.678 0 0 1 .195-.6l1.052-1.025-1.453-.212a.678.678 0 0 1-.51-.37L12.25 8.21l-.65 1.317Z" fill="#fff"/><path d="M6.5 2A2.5 2.5 0 0 0 4 4.5v15A2.5 2.5 0 0 0 6.5 22h13.25a.75.75 0 0 0 0-1.5H6.5a1 1 0 0 1-1-1h14.25a.75.75 0 0 0 .75-.75V4.5A2.5 2.5 0 0 0 18 2H6.5ZM19 18H5.5V4.5a1 1 0 0 1 1-1H18a1 1 0 0 1 1 1V18Z" fill="#fff"/></svg>
		</div>
		<div class="flex  justify-center mt-2 mx-auto p-3 rounded-lg hover:bg-blue-700 transition-all cursor-pointer">
			<svg width="34" height="34" fill="none" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"
				><path
					d="M6.19 21.854a.75.75 0 0 1-1.188-.61V6.25a3.25 3.25 0 0 1 3.25-3.25h7.499A3.25 3.25 0 0 1 19 6.249v14.996a.75.75 0 0 1-1.188.609l-5.811-4.181-5.812 4.18Z"
					fill="#fff"
				/></svg
			>
		</div>
	{:else if selected === 3}
		<div class="flex  justify-center mt-10 mx-auto p-3 rounded-lg  hover:bg-blue-700 transition-all cursor-pointer">
			<svg width="24" height="24" fill="none" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M10.55 2.532a2.25 2.25 0 0 1 2.9 0l6.75 5.692c.507.428.8 1.057.8 1.72v9.803a1.75 1.75 0 0 1-1.75 1.75h-3.5a1.75 1.75 0 0 1-1.75-1.75v-5.5a.25.25 0 0 0-.25-.25h-3.5a.25.25 0 0 0-.25.25v5.5a1.75 1.75 0 0 1-1.75 1.75h-3.5A1.75 1.75 0 0 1 3 19.747V9.944c0-.663.293-1.292.8-1.72l6.75-5.692Zm1.933 1.147a.75.75 0 0 0-.966 0L4.767 9.37a.75.75 0 0 0-.267.573v9.803c0 .138.112.25.25.25h3.5a.25.25 0 0 0 .25-.25v-5.5c0-.967.784-1.75 1.75-1.75h3.5c.966 0 1.75.783 1.75 1.75v5.5c0 .138.112.25.25.25h3.5a.25.25 0 0 0 .25-.25V9.944a.75.75 0 0 0-.267-.573l-6.75-5.692Z" fill="#fff"/></svg>
		</div>

		<div
			on:click={() => {
				goto('');
			}}
			class="flex  justify-center mt-2 mx-auto p-3 rounded-lg hover:bg-blue-700 transition-all cursor-pointer"
		>
		<svg width="24" height="24" fill="none" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="m10.542 8.608 1.1-2.23a.678.678 0 0 1 1.216 0l1.1 2.23 2.461.357c.556.08.778.764.376 1.157l-1.78 1.735.42 2.45a.678.678 0 0 1-.984.716l-2.201-1.157-2.2 1.157a.678.678 0 0 1-.985-.715l.42-2.45-1.78-1.736a.678.678 0 0 1 .376-1.157l2.46-.357Zm1.058.92a.678.678 0 0 1-.51.37l-1.454.212 1.052 1.025c.16.156.232.38.195.6l-.249 1.448 1.3-.684a.678.678 0 0 1 .632 0l1.3.684-.249-1.448a.678.678 0 0 1 .195-.6l1.052-1.025-1.453-.212a.678.678 0 0 1-.51-.37L12.25 8.21l-.65 1.317Z" fill="#fff"/><path d="M6.5 2A2.5 2.5 0 0 0 4 4.5v15A2.5 2.5 0 0 0 6.5 22h13.25a.75.75 0 0 0 0-1.5H6.5a1 1 0 0 1-1-1h14.25a.75.75 0 0 0 .75-.75V4.5A2.5 2.5 0 0 0 18 2H6.5ZM19 18H5.5V4.5a1 1 0 0 1 1-1H18a1 1 0 0 1 1 1V18Z" fill="#fff"/></svg>
		</div>
		<div class="flex  justify-center mt-2 mx-auto p-3 rounded-lg bg-blue-600 hover:bg-blue-700 transition-all cursor-pointer">
			<svg width="34" height="34" fill="none" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"
				><path
					d="M6.19 21.854a.75.75 0 0 1-1.188-.61V6.25a3.25 3.25 0 0 1 3.25-3.25h7.499A3.25 3.25 0 0 1 19 6.249v14.996a.75.75 0 0 1-1.188.609l-5.811-4.181-5.812 4.18Z"
					fill="#fff"
				/></svg
			>
		</div>
	{/if}

	<!--List İtems-->
</div>
