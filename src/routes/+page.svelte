<script lang="ts">

	import { browser } from '$app/environment';
 
	let isDarkMode: any;

	if (browser) {
		let mediaQueryObj = window.matchMedia('(prefers-color-scheme: dark)');
		isDarkMode = mediaQueryObj.matches;
	}

	console.log(isDarkMode);

</script>

<div class="hero min-h-screen">
  <div class="hero-content text-center">
    <div class="max-w-md prose">
      <h1 class="text-5xl font-bold mt-[-300px]">Challenges of Feeding a Growing Planet</h1>
      <div class="flex justify-between w-[1000px] ml-[-290px]">
		<a class="flex flex-col w-96" href="part1">
			<h2>Part 1</h2>
			{#if isDarkMode}
				<img src="/p1Dark.png" alt="Screenshot of Part 1" class="w-96">
			{:else}
				<img src="/p1Light.png" alt="Screenshot of Part 1" class="w-96">
			{/if}
		</a>
		<a class="flex flex-col w-96" href="part2">
			<h2>Part 2</h2>
			{#if isDarkMode}
				<img src="/p2Dark.png" alt="Screenshot of Part 2" class="w-96">
			{:else}
				<img src="/p2Light.png" alt="Screenshot of Part 2" class="w-96">
			{/if}
		</a>
	  </div>
    </div>
  </div>
</div>

<style>

		img {
		border-color: #7FD87B;
		border-width: 3px;
		border-radius: 1rem;
	}

</style>