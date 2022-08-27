<script>
	import { goto } from '$app/navigation';

	export /**
	 * @type {number}
	 */
	let selected;
</script>

<div class="h-screen w-20 bg-gradient-to-b from-[#12141d41] to-[#37427200]  flex flex-col fixed">
	{#if selected === 1}
		<div class="flex  justify-center mt-10 mx-auto p-3 rounded-lg bg-blue-600 hover:bg-blue-700 transition-all  cursor-pointer">
			<svg width="34" height="34" fill="none" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"
				><path
					d="M10.55 2.533a2.25 2.25 0 0 1 2.9 0l6.75 5.695c.508.427.8 1.056.8 1.72v9.802a1.75 1.75 0 0 1-1.75 1.75h-3a1.75 1.75 0 0 1-1.75-1.75v-5a.75.75 0 0 0-.75-.75h-3.5a.75.75 0 0 0-.75.75v5a1.75 1.75 0 0 1-1.75 1.75h-3A1.75 1.75 0 0 1 3 19.75V9.947c0-.663.292-1.292.8-1.72l6.75-5.694Z"
					fill="#fff"
				/></svg
			>
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
			<svg width="34" height="34" fill="none" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"
				><path
					d="M10.55 2.533a2.25 2.25 0 0 1 2.9 0l6.75 5.695c.508.427.8 1.056.8 1.72v9.802a1.75 1.75 0 0 1-1.75 1.75h-3a1.75 1.75 0 0 1-1.75-1.75v-5a.75.75 0 0 0-.75-.75h-3.5a.75.75 0 0 0-.75.75v5a1.75 1.75 0 0 1-1.75 1.75h-3A1.75 1.75 0 0 1 3 19.75V9.947c0-.663.292-1.292.8-1.72l6.75-5.694Z"
					fill="#fff"
				/></svg
			>
		</div>

		<div
			on:click={() => {
				goto('');
			}}
			class="flex  justify-center mt-2 mx-auto p-3 rounded-lg bg-blue-600 hover:bg-blue-700 transition-all cursor-pointer"
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
	{:else if selected === 3}
		<div class="flex  justify-center mt-10 mx-auto p-3 rounded-lg  hover:bg-blue-700 transition-all cursor-pointer">
			<svg width="34" height="34" fill="none" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"
				><path
					d="M10.55 2.533a2.25 2.25 0 0 1 2.9 0l6.75 5.695c.508.427.8 1.056.8 1.72v9.802a1.75 1.75 0 0 1-1.75 1.75h-3a1.75 1.75 0 0 1-1.75-1.75v-5a.75.75 0 0 0-.75-.75h-3.5a.75.75 0 0 0-.75.75v5a1.75 1.75 0 0 1-1.75 1.75h-3A1.75 1.75 0 0 1 3 19.75V9.947c0-.663.292-1.292.8-1.72l6.75-5.694Z"
					fill="#fff"
				/></svg
			>
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
