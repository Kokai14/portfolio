<script lang="ts">
	import Header from '../Header.svelte';
</script>

<div>
	<Header />
	<div class="university">
		<div>
			<p class="text">I am a first year student at innopolis university.</p>
			<p class="text">I am studying computer science with</p>
			<p class="text">specalitiy in software development</p>
		</div>
		<img
			id="univerity-img"
			src="https://thumbs.dreamstime.com/b/modern-building-innopolis-university-russia-june-city-republic-tatarstan-119068181.jpg"
			alt="university"
		/>
	</div>
</div>

<style>
	#univerity-img {
		width: 500px;
		height: 350px;
		margin-left: 250px;
		margin-bottom: 100px;
	}
	div {
		background-color: #51a878;
	}
	.text {
		font-size: 30px;
		margin-left: 40px;
		width: fit-content;
		font-family: 'Caveat', cursive;
	}
	.university {
		display: flex;
	}
</style>
