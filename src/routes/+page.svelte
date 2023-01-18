<script>
	import BeInspired from '@/components/BeInspired.svelte'
	import HeroImg from '@/components/HeroImg.svelte'
	import ImageGrid1 from '@/components/ImageGrid1.svelte'
	import ImageGrid2 from '@/components/ImageGrid2.svelte'
	import ImageGrid3 from '@/components/ImageGrid3.svelte'
	import LinkButton from '@/components/LinkButton.svelte'
</script>

<div class="container">
	<div class="content">
		<HeroImg />
		<header>
			<h1 class="heading-xl">modern<br /> art gallery</h1>
			<p>
				The arts in the collection of the Modern Art Gallery all started from a spark of
				inspiration. Will these pieces inspire you? Visit us and find out.
			</p>
			<div class="link-button">
				<LinkButton direction={'right'} href="/location">our location</LinkButton>
			</div>
		</header>
		<main>
			<div class="image-grid-1">
				<ImageGrid1 />
			</div>

			<div class="introduction">
				<h2 class="heading-l mobile">your day<br /> at the gallery</h2>
				<h2 class="heading-l desktop">your day at<br /> the gallery</h2>
				<p>
					Wander through our distinct collections and find new insights about our artists. Dive into
					the details of their creative process.
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
	</div>

	<footer>
		<img src="/images/logo-light.svg" alt="" />
		<p>
			The Modern Art Gallery is free to all visitors and open seven days a week from 8am to 9pm.
			Find us at 99 King Street, Newport, USA.
		</p>
		<div class="social-media">
			<img src="/images/icon-facebook.svg" alt="facebook" />
			<img src="/images/icon-instagram.svg" alt="instagram" />
			<img src="/images/icon-twitter.svg" alt="twitter" />
		</div>
	</footer>
</div>

<style lang="scss">
	.container {
		position: relative;
		min-height: 100vh;

		.content {
			header {
				padding: 2rem 1rem 7.5rem;

				p {
					padding: 2rem 0;
				}

				.link-button {
					max-width: 260px;
				}
			}

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
		}

		footer {
			position: absolute;
			background-color: var(--color-almost-black);
			padding: 3rem 2rem;
			margin-top: 5rem;
			bottom: 0;
			width: 100%;

			p {
				color: var(--color-white);
				font-size: var(--fs-small);
				line-height: var(--lh-small);
				padding: 2.37rem 0;
			}

			.social-media {
				display: flex;
				gap: 1.5rem;
			}
		}
	}
</style>
