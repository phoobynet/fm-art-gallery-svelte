<script lang="ts">
	import LinkButton from '@/components/LinkButton.svelte'
</script>

<header>
	<div class="hero">
		<picture>
			<source
				srcset={`/images/desktop/image-hero.jpg, /images/desktop/image-hero@2x.jpg 2x`}
				media="(min-width:1440px)"
				alt=""
			/>

			<source
				srcset={`/images/tablet/image-hero.jpg, /images/tablet/image-hero@2x.jpg 2x`}
				media="(min-width:768px)"
				alt=""
			/>

			<source
				srcset={`/images/mobile/image-hero.jpg, /images/mobile/image-hero@2x.jpg 2x`}
				media="(min-width:375px)"
				alt=""
			/>
			<img src="/images/mobile/image-hero.jpg" alt="" />
		</picture>
	</div>
	<div class="content">
		<h1 class="heading-xl">modern<br /> art gallery</h1>
		<p>
			The arts in the collection of the Modern Art Gallery all started from a spark of inspiration.
			Will these pieces inspire you? Visit us and find out.
		</p>
		<div class="link-button">
			<LinkButton direction={'right'} href="/location">our location</LinkButton>
		</div>
	</div>
</header>

<style lang="scss">
	header {
		display: grid;
		grid-template-areas:
			'hero'
			'content';

		.hero {
			grid-area: hero;
		}

		.content {
			display: grid;
			grid-row-gap: 2rem;
			grid-area: content;
			padding: 2rem 1rem 7.5rem 1rem;

			.link-button {
				max-width: 260px;
			}
		}

		@media (min-width: 768px) {
			grid-template-columns: auto 3rem auto;
			grid-template-areas: 'hero middle content';

			.hero {
				grid-column: hero / middle-end;
				width: 437px;
			}

			.content {
				grid-column: middle / content;
				place-self: center;
				padding: 0 2rem 0 0;
				grid-gap: 3rem;
			}
		}
	}
</style>
