<script>
	let communities = [
		{
			name: 'Veiversa Studio',
			description:
				'Veiversa Studio is a fast and original software group. We are passionate about software development and we are always looking for new ideas and technologies. We are a team of creative and talented people who are always ready to help you.',
			image: 'https://cdn.discordapp.com/icons/892759653421809745/824b08bbd98bc8b411a12927a4ffb089.webp',
			members_length: 4,
			website: 'https://veiversa.github.io'
		},
		{
			name: 'Vezalan Software',
			description:
				'Vezalan Software is a software company with currently 8 members. Most prefered languages among the company is C#, JavaScript and PHP.',
			image: 'https://cdn.discordapp.com/icons/794275803935932446/055f1ac0e3ae6c851ad06a58c2835836.webp',
			members_length: 22,
			website: 'https://vezalansoftware.com'
		}
	];
</script>

<main class="container" id="communities">
	<h2 class="text-gray-200 text-4xl my-10 font-semibold">Communities</h2>
	<div class="flex flex-col items-center space-y-10">
		{#each communities as community}
			<a href={community.website} target="_blank" class="w-full">
				<div class="bg-[#10151cac] hover:bg-[#0d1117] transition-all rounded-lg w-full md:flex p-2 shadow-lg">
					<img src={community.image} class="rounded-xl hidden md:block" alt="" />
					<div class="pl-5 pr-2">
						<h3 class="text-gray-200 text-xl font-bold py-1 ">{community.name}</h3>
						<p class="text-gray-400">{community.description}</p>
						<p class="py-2 text-gray-300">👥 {community.members_length}</p>
					</div>
				</div></a
			>
		{/each}
	</div>
</main>
