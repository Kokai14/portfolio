<script lang="ts">
	import { formatDistanceToNow } from 'date-fns';
	import { onMount } from 'svelte';
	interface Data {
		month: number;
		num: number;
		link: string;
		year: number;
		news: string;
		safe_title: string;
		transcript: string;
		alt: string;
		img: string;
		title: string;
		day: number;
	}
	let img: HTMLImageElement;
	let title: HTMLParagraphElement;
	let timeTillNow: HTMLParagraphElement;
	let date: HTMLParagraphElement;
	onMount(async () => {
		async function fetchXKCD(): Promise<string | null> {
			const urlParams = new URLSearchParams();
			urlParams.append('email', 'k.khaddour@innopolis.university');
			try {
				const response = await fetch(
					'https://fwd.innopolis.university/api/hw2?' + urlParams.toString()
				);
				const data: string = await response.json();
				return data;
			} catch (error) {
				console.error('Error fetching comic identifier:', error);
				return null;
			}
		}

		try {
			const id: string | null = await fetchXKCD();
			if (id == null) {
				throw Error('Not able to fetch ID');
			}
			const response = await fetch(`https://fwd.innopolis.university/api/comic?id=${id}`);
			const _data: Data = await response.json();
			img.src = _data.img;
			img.alt = _data.alt;
			title.textContent = _data.safe_title;
			const event = new Date(Date.UTC(_data.year, _data.month, _data.day));
			timeTillNow.textContent = 'it was published ' + formatDistanceToNow(event) + ' ago';
			const options: Intl.DateTimeFormatOptions = {
				year: 'numeric',
				month: 'long',
				day: 'numeric'
			};
			date.textContent = event.toLocaleDateString('en-DE', options);
		} catch (error) {
			console.error('Error fetching comic identifier:', error);
		}
	});
</script>

<div>
	<section id="joke">
		<img bind:this={img} id="img" src="/" alt="" />
		<p bind:this={title} id="title" class="text" />
		<p bind:this={timeTillNow} id="timeTillNow" class="text" />
		<p bind:this={date} id="date" class="text" />
	</section>
</div>

<style>
	section {
		background-color: #51a878;
	}
	#joke {
		padding: 0 10%;
		height: 80vh;
		display: flex;
		flex-direction: column;
		align-items: center;
	}
	#img {
		min-width: 100px;
		min-height: 100px;
		display: block;
		text-align: center;
		font-size: larger;
	}
	.text {
		font-size: 30px;
		margin: auto;
		width: fit-content;
		padding: 10px;
		font-family: 'Caveat', cursive;
	}
	#img {
		border: '10px solid orange';
		padding: '10px';
	}
</style>
