<script lang="ts">
	import Header from '../Header.svelte';
</script>

<div>
	<Header />
	<div class="ping-pong">
		<div>
			<p class="text">I have started playing tabel tennis</p>
			<p class="text">ten months ago. I play it almost every day,</p>
			<p class="text">and I have participated in many mini tournements</p>
		</div>
		<img
			id="pingpong-img"
			src="https://www.southdownsleisure.co.uk/wp-content/uploads/2019/02/Table-Tennis-1000x1000-600x600.jpg"
			alt="university"
		/>
	</div>
</div>

<style>
	div {
		background-color: #51a878;
	}
	.ping-pong {
		display: flex;
	}
	#pingpong-img {
		width: 350px;
		height: 350px;
		margin-left: 350px;
		margin-bottom: 100px;
	}
	.text {
		font-size: 30px;
		margin: auto;
		width: fit-content;
		padding: 10px;
		font-family: 'Caveat', cursive;
	}
</style>
