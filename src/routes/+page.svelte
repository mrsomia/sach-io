<script>
	import GitHubIcon from '$lib/GitHubIcon.svelte';

	let projectLinks = [
		{
			name: 'Cash Game Calculator',
			link: 'https://cash-game.vercel.app/',
      github: 'https://github.com/mrsomia/cash-game'
		},
		{
			name: 'Splash',
			link: 'https://splash-pong.vercel.app/',
			github: 'https://github.com/mrsomia/splash'
		},
		{
			name: 'Golf Card',
			link: 'https://golf-card.netlify.app/',
			github: 'https://github.com/mrsomia/golf-card'
		},
		{
			name: 'Drunk Math',
			link: 'https://drunk-math.vercel.app/',
			github: 'https://github.com/mrsomia/drunk-math'
		}
	];
</script>

<svelte:head>
	<title>Sachin Somia</title>
	<meta name="description" content="A web developer that likes javascript typescript and go. Based in Cork" />
</svelte:head>

<main class="px-6 py-6 mx-auto sm:max-w-screen-sm text-white">
	<h1 class="text-2xl font-semibold py-2 text-orange-500">Sachin Somia</h1>
	<p class="py-2">👋 Hi, I'm Sachin Somia, but most people call me Sach. I like making web apps.</p>
	<p class="py-2">
		You can find me on <a
			class="underline underline-offset-2 text-orange-600"
			href="https://github.com/mrsomia">Github</a
		>
	</p>
	<p class="py-2">Here's some things I worked on.</p>
	<h2 class="text-xl py-2 font-medium">Projects</h2>
	<ul class="space-y-2">
		{#each projectLinks as link}
			<li class="">
				<div class="flex space-x-2">
					<a class="underline underline-offset-2 text-orange-500" href={link.link}>{link.name}</a>
					{#if link.github} 
						<div class="w-5">
							<a href={link.github}>
								<GitHubIcon />
							</a>
						</div>
					{/if}
				</div>
			</li>
		{/each}
	</ul>
</main>
