<script>
</script>

<div>
	<div class="bgContainer">
		<video autoplay loop muted playsinline class="backgroundVideo">
			<source
				src="https://res.cloudinary.com/mykeld74/video/upload/v1687021864/zimbabwe/PenielBg.mp4"
				type="video/mp4"
			/>
		</video>
		<div class="overlay" />
	</div>

	<div class="mainContainer">
		<div class="mainContent">
			<h1 class="headline">
				Providing food, family, education, hope and Christ to those who need it most.
			</h1>
			<h2 class="subhead">Peniel Centre and Hillside</h2>
		</div>
	</div>
</div>

<style>
	.bgContainer {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		z-index: -1;
		pointer-events: none;
	}
	.backgroundVideo {
		position: fixed;
		right: 0;
		bottom: 0;
		min-width: 100%;
		min-height: 100%;
		z-index: -1;
	}
	.overlay {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		pointer-events: none;
		/* background-color: rgba(0,0,0,0.5); */
		background-image: linear-gradient(
			to bottom,
			rgba(255, 255, 255, 0.6),
			rgba(255, 255, 255, 0.3)
		);
		z-index: -1;
	}
	.mainContainer {
		display: flex;
		justify-content: center;
		align-items: center;
		width: 100%;
		min-height: calc(100vh - 170px);
		text-align: center;
	}
</style>
