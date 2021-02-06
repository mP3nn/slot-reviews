<script>
	export let name;
	export let rating;
	export let logo;
	export let intro;
	export let image1;
	export let description2;
	export let image2;

	
	let readMore = false
	
	function onReadMore() {
		readMore = !readMore
	}
</script>

<div class="card">
	<div class="row">
		<img src="{logo}" alt="" style="width:20%;">
		<div class="col-9">
			<span><h1> {name} </h1><img src="{rating}" alt="" style="width:30%;"> </span>
		</div>
		<div class="col-3">
			{#if !readMore}<button class="button-primary" on:click={onReadMore}>Read More</button>{:else}<button class="button-danger" on:click={onReadMore}>Read Less</button>{/if}
		</div>
	</div>
	{#if readMore}
		<img src="{image1}" class="border-radius my-2" alt="">
		<h2>Introduzione</h2>
		<p class="my-2">{intro}</p>
		<img src="{image2}" class="border-radius my-2" alt="">
		<h2>Selezione di Giochi</h2>
		<p class="my-2">{description2[0].g_selection}</p>
		<h2>Sito Web</h2>
		<p class="my-2">{description2[0].site}</p>
		<h2>Bonus e Spin gratuiti</h2>
		<p class="my-2">{description2[0].bonuses}</p>
		<h2>Conclusioni</h2>
		<p class="my-2">{description2[0].conclusion}</p>
	{/if}
</div>