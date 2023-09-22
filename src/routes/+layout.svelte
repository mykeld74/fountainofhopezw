<script>
	import { fade } from 'svelte/transition';
	import '$css/reset.css';
	import '$css/styles.css';
	import Image from '$components/Image.svelte';
	import Navbar from '$components/Navbar.svelte';

	export let data;
</script>

<svelte:head>
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
	<link
		href="https://fonts.googleapis.com/css2?family=Manrope:wght@200;300;400;500;600;700;800&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

<header>
	<div class="headerContainer">
		<div class="imageContainer">
			<a href="/">
				<Image
					source="zimFlag"
					altText="Peniel Centre and Hillside"
					width="200"
					classes="header-image"
				/>
			</a>
		</div>
		<div class="headerText">
			<p class="headline">Fountain of Hope</p>
			<p class="subhead">Peniel Centre and Hillside</p>
		</div>
	</div>
	<Navbar />
</header>
{#key data.pathname}
	<div in:fade={{ duration: 150, delay: 150 }} out:fade={{ duration: 150 }}>
		<slot />
	</div>
{/key}

<style>
	.headerContainer {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 20px;
		background: transparent;
	}
	.headline {
		font-size: clamp(24px, 5vw, 48px);
		font-weight: 900;
		margin: 0;
	}
	.subhead {
		font-size: clamp(18px, 3.5vw, 30px);
		font-weight: 500;
		margin: 0;
	}
	.imageContainer {
		width: 15vw;
		max-width: 100px;
	}
</style>
