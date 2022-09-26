<script>
	import jquery from 'jquery';

	jquery(document).ready(function () {
		jquery(window).scroll(function () {
			const scroll = jquery(window).scrollTop();

			if (scroll > 100) {
				jquery('#goHome').fadeIn(200);
			} else {
				jquery('#goHome').fadeOut(200);
			}
		});
	});
</script>

<main
	on:click={() => {
		jquery('html, body').animate({ scrollTop: 0 }, 100);
	}}
	class="fixed right-5 bottom-5 hidden"
	id="goHome"
>
	<div class="h-10 w-10 bg-gray-800 flex items-center justify-center rounded-lg shadow-lg cursor-pointer">
		<svg width="24" height="24" fill="none" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"
			><path
				d="M4.284 10.296A1 1 0 0 0 5.709 11.7L11 6.33V20a1 1 0 1 0 2 0V6.336l5.285 5.364a1 1 0 0 0 1.425-1.404l-6.823-6.924a1.25 1.25 0 0 0-1.78 0l-6.823 6.924Z"
				fill="#fff"
			/></svg
		>
	</div>
</main>
