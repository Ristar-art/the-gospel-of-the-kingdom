<script lang="ts">
	import hero from '$lib/images/hero.svg';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section
	class="h-screen flex items-center justify-center">
  <!-- <h1 class="text-white text-4xl">Welcome to My Starry Sky Landing Page</h1> -->

	<h1  class="text-white text-4xl">
		<span class="welcome">
			<picture>
				<img src={hero} alt="goslel illastration" class="w-[2em] h-[2em]" />
			</picture>
		</span>

		This gospel of the kingdom will be  <br /> preached in the whole world 

	</h1>

	<h2  class="text-white ">
		 <strong>Matthew 24:14</strong>
	</h2>	
</section>
<section>

</section>

<style>
	
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
</style>
