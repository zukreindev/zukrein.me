<script>
	/**
	 * @type {any[]}
	 */
	let repo;
	fetch('https://api.github.com/users/ardasamedcelik/repos').then(async (e) => {
		// @ts-ignore

		repo = e.json();

		console.log(repo);
	});
</script>

<main>
	{JSON.stringify(repo)}
</main>
