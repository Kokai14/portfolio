<script lang="ts">
	import Header from '../Header.svelte';
</script>

<svelte:head>
	<script src="https://kit.fontawesome.com/dbee5ef51c.js" crossorigin="anonymous"></script>
</svelte:head>

<div>
	<Header />
	<p class="text">I would love to hear from you</p>
	<p class="text">you can contact me in the following platforms</p>
	<div class="icons">
		<a href="https://www.linkedin.com/in/karam-khaddour-739436263/"
			><i id="ld-link" class="fa fa-linkedin" /></a
		>
		<a href="https://t.me/karamkhaddour"><i id="tg-link" class="fa fa-telegram" /></a>
		<a href="https://www.facebook.com/karam.khaddour.370?mibextid=ZbWKwL"
			><i id="fb-link" class="fa fa-facebook" /></a
		>
	</div>
</div>

<style>
	div {
		background-color: #51a878;
	}
	.text {
		font-size: 30px;
		margin: auto;
		width: fit-content;
		padding: 10px;
		font-family: 'Caveat', cursive;
	}

	.icons {
		font-size: larger;
		margin: auto;
		width: fit-content;
	}
</style>
