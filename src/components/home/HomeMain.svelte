<script>
	import BeInspired from '@/components/home/BeInspired.svelte'
	import ImageGrid1 from '@/components/home/ImageGrid1.svelte'
	import ImageGrid2 from '@/components/home/ImageGrid2.svelte'
	import ImageGrid3 from '@/components/home/ImageGrid3.svelte'
</script>

<main>
	<div class="image-grid-1">
		<ImageGrid1 />
	</div>

	<div class="introduction">
		<h2 class="heading-l mobile">your day<br /> at the gallery</h2>
		<h2 class="heading-l desktop">your day at<br /> the gallery</h2>
		<p>
			Wander through our distinct collections and find new insights about our artists. Dive into the
			details of their creative process.
		</p>
	</div>

	<div class="image-grid-2">
		<ImageGrid2 />
	</div>
	<div class="image-grid-3">
		<ImageGrid3 />
	</div>
	<div class="be-inspired">
		<BeInspired />
	</div>
</main>

<style lang="scss">
	main {
		display: grid;
		padding: 0 1rem;
		grid-template-rows: repeat(5, auto);
		grid-template-areas:
			'image-grid-1'
			'introduction'
			'image-grid-2'
			'image-grid-3'
			'be-inspired';
		grid-row-gap: 1rem;

		.introduction {
			padding: 1rem 0;
			grid-area: introduction;

			h2 {
				padding-bottom: 1rem;

				&.desktop {
					display: none;
				}
			}
		}

		.image-grid-1 {
			grid-area: image-grid-1;
		}

		.image-grid-2 {
			grid-area: image-grid-2;
			height: 480px;
		}

		.image-grid-3 {
			grid-area: image-grid-3;
		}

		.be-inspired {
			grid-area: be-inspired;
		}

		@media (min-width: 768px) {
			grid-template-columns: 40% 20% 40%;
		}

		@media (min-width: 1440px) {
			.introduction {
				h2 {
					&.mobile {
						display: none;
					}

					&.desktop {
						display: block;
					}
				}
			}
		}
	}
</style>
