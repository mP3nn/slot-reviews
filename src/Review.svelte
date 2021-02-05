<script>
	export let name;
	export let rating;
	export let description1;
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
		<div class="col-9">
			<h1>{name} {rating}</h1>
		</div>
		<div class="col-3">
			{#if !readMore}<button class="button-primary" on:click={onReadMore}>Read More</button>{:else}<button class="button-danger" on:click={onReadMore}>Read Less</button>{/if}
		</div>
	</div>
	{#if readMore}
		<p class="my-2">{description1}</p>
		<img src="{image1}" class="border-radius my-2" alt="">
		<p class="my-2">{description2}</p>
		<img src="{image2}" class="border-radius my-2" alt="">
	{/if}
</div>