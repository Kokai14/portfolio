<script lang="ts">
	import { base } from '$app/paths';
</script>

<footer id="list">
	<ul>
		<li id="item1"><a href="{base}/bio">bio</a></li>
		<li id="item2"><a href="{base}/education">education</a></li>
		<li id="item3"><a href="{base}/hobbies">hobbies</a></li>
		<li id="item4"><a href="{base}/contacts">contacts</a></li>
		<li id="item5"><a href="{base}/comic">Do you want a joke</a></li>
	</ul>
</footer>

<style>
	#list {
		text-align: center;
	}
	ul {
		display: inline-block;
		list-style-type: none;
	}
	li {
		display: inline;
	}
	#item1 {
		margin-right: 25px;
	}
	#item2 {
		margin-left: 25px;
		margin-right: 25px;
	}
	#item3 {
		margin-left: 25px;
		margin-right: 25px;
	}
	#item4 {
		margin-left: 25px;
		margin-right: 25px;
	}
	#item5 {
		margin-left: 25px;
	}
	a:link {
		color: rgb(73, 77, 73);
		background-color: transparent;
		text-decoration: none;
	}
	a:visited {
		color: rgb(73, 77, 73);
		background-color: transparent;
		text-decoration: none;
	}
	a:hover {
		color: black;
		background-color: transparent;
		text-decoration: underline;
	}
</style>
