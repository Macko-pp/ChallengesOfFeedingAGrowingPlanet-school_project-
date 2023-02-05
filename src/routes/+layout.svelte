<script>
	import '../app.postcss';
</script>

<svelte:head>

	<script src="https://kit.fontawesome.com/7c7d59d412.js" crossorigin="anonymous"></script>

</svelte:head>

<div class="navbar bg-slate-100 dark:bg-slate-800">
	<div class="flex-none">
		<a href="/">
			<btn class="btn btn-square btn-ghost hover:bg-transparent spin">
				<img src="/Tree.png" alt="tree">
			</btn>
		</a>
	</div>
	<div class="flex-1">
		<a href="/">
			<button class="btn btn-ghost normal-case text-xl">Challenges of Feeding a Growing Planet</button>
		</a>
	</div>
	<div class="flex-none">
		<ul class="menu menu-horizontal p-0">
			<li><a class="btn btn-ghost text-base rounded-lg" href="part1">Part 1</a></li>
			<li><a class="btn btn-ghost text-base rounded-lg" href="part2">Part 2</a></li>
		</ul>
	</div>

	<div class="dropdown dropdown-end flex-none">
		<button tabindex="0" class="btn btn-ghost bg-[#7FD87B]">
			<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" class="inline-block w-5 h-5 stroke-current dark:stroke-white">
				<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 12h.01M12 12h.01M19 12h.01M6 12a1 1 0 11-2 0 1 1 0 012 0zm7 0a1 1 0 11-2 0 1 1 0 012 0zm7 0a1 1 0 11-2 0 1 1 0 012 0z"></path>
			</svg>
		</button>
		<ul class="dropdown-content menu p-2 shadow bg-base-100 rounded-box w-52">
			<li><a href="https://github.com/Macko-pp/ChallengesOfFeedingAGrowingPlanet-school_project-"><i class="fa-brands fa-github left-0"></i>Source Code</a></li>
			<li><a href="https://docs.google.com/document/d/1sDCqFK--S71HJey5Y3_fk-ukV7raDMlKIOAjtoipli0/edit?usp=sharing"><i class="fa-solid fa-file"></i>Sources</a></li>
		</ul>
	</div>
</div>

<div class="padded">
	<slot />
</div>

<style>
	.navbar {
		position: fixed;
		z-index: 1;
	}

	@keyframes spin {
		0% {
			transform: rotate(0);
		}

		100% {
			transform: rotate(360deg);
		}
	}

	.spin {
		animation: spin 1s ease 0s 1 normal forwards;
	}

	.padded {
		padding: 3.33rem;
		padding-top: 7.6rem;
	}
</style>