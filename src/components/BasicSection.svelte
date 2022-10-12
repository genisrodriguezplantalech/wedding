<script>
	import { openNewWindow } from './../utils';
	export let titleIconChurch = false;
	export let titleIconList = false;
	export let titleIconMusic = false;
	export let songs = false;
	export let title = undefined;
	export let description = undefined;
	export let buttonText = undefined;
	export let buttonExternalUrl = undefined;

	const openExternalUrl = () => openNewWindow(buttonExternalUrl);
</script>

<div class="g__section">
	{#if titleIconChurch}
		<i class="fa fa-church"></i>
	{:else if titleIconList}
		<i class="fas fa-clipboard-list"></i>
	{:else if titleIconMusic}
		<i class="fas fa-music"></i>
	{/if}
	<h1>{title}</h1>
	<p class="text">{description}</p>
	{#if songs}
		<a href="https://www.youtube.com/watch?v=zczXXe90vCM">A Million Dreams - The Greatest Showman</a>
	{/if}
	<button class="g__button" on:click={openExternalUrl}>
		{buttonText}
	</button>
</div>

<style>
	i {
		font-size: 3rem;
	}
	a{
		padding-bottom: 50px;
		color: white;
	}
</style>
