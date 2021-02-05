<script>
	import Review from "./Review.svelte"
	
	let reviews = [
		
	];
	
	let homePage = true;
	let reviewsPage = false;
	
	function goHomePage() {
		homePage = true;
		reviewsPage = false;
	}
	function goReviewsPage() {
		homePage = false;
		reviewsPage = true;
	}
</script>

<div class="row dark">
	<div class="col-10">
		<span class="navbar-logo" on:click={goHomePage}>Shark Review</span>
	</div>
	<div class="col-1">
		<span class="navbar-link" on:click={goHomePage}>Home</span>
	</div>
	<div class="col-1">
		<span class="navbar-link" on:click={goReviewsPage}>Reviews</span>
	</div>
</div>

<div class="container">
	{#if homePage}
		<div class="card">
			<div class="row">
				<div class="col-12">
					<img src="./img/logo.png" style="width:100px; margin-left:auto; margin-right:auto; display:block" alt="">
				</div>
				<div class="col-12">
					<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam commodo velit vitae est consequat, quis elementum mauris pretium. Vivamus suscipit et elit ut varius. Nunc varius libero sed metus fermentum, vitae interdum ligula ornare. Ut quis orci eget erat placerat gravida. Mauris ut aliquam mauris. Vestibulum sit amet porttitor dui, quis tristique odio. Nulla consequat orci in lacus sagittis, ac egestas enim aliquet. Proin condimentum nulla lacus, et convallis quam tincidunt sit amet. Nulla tincidunt turpis eu lorem efficitur venenatis. Integer libero enim, consectetur et molestie ut, faucibus vitae metus. Nam tempus feugiat vehicula.</p>
				</div>
				<div class="col-12">
					<h1 class="text-center">Le migliori Slot</h1>
				</div>
				<div class="col-4">
					<div class="card">
						<h1>Slot 1</h1>
						<img class="border-radius my-1" src="https://mmseagames2013.com/wp-content/uploads/2020/01/8909273.jpg" alt="">
						<button class="button-success">Leggi di più</button>
					</div>
				</div>
				<div class="col-4">
					<div class="card">
						<h1>Slot 2</h1>
						<img class="border-radius my-1" src="https://mmseagames2013.com/wp-content/uploads/2020/01/8909273.jpg" alt="">
						<button class="button-success">Leggi di più</button>
					</div>
				</div>
				<div class="col-4">
					<div class="card">
						<h1>Slot 3</h1>
						<img class="border-radius my-1" src="https://mmseagames2013.com/wp-content/uploads/2020/01/8909273.jpg" alt="">
						<button class="button-success">Leggi di più</button>
					</div>
				</div>
			</div>
		</div>
	{/if}

	{#if reviewsPage}
		<div class="card">
			<h1 class="text-center">Reviews</h1>
		</div>

		{#each reviews as review}
			<Review name={review.name} rating={review.rating} description1={review.description1} image1={review.image1} description2={review.description2} image2={review.image2}/>
		{/each}
	{/if}
</div>

<div class="light">
	<div class="container">
		<img src="./img/18.png" alt="" class="py-1" style="display: block; margin-left: auto; margin-right: auto; width: 50px;">
		<h4 class="py text-center">Disclaimer AAMS & Probabilità di Vincita</h4>
		<p class="py text-center">© 2021 Slot Review. All rights reserved.</p>
	</div>
</div>