<main>
	<div class="image-grid-1">
		<picture>
			<source
				srcset={`/images/desktop/image-grid-1.jpg, /images/desktop/image-grid-1@2x.jpg 2x`}
				media="(min-width:1440px)"
				alt=""
			/>

			<source
				srcset={`/images/tablet/image-grid-1.jpg, /images/tablet/image-grid-1@2x.jpg 2x`}
				media="(min-width:768px)"
				alt=""
			/>

			<source
				srcset={`/images/mobile/image-grid-1.jpg, /images/mobile/image-grid-1@2x.jpg 2x`}
				media="(min-width:375px)"
				alt=""
			/>
			<img src="/images/mobile/image-grid-1.jpg" alt="" />
		</picture>
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
		<picture>
			<source
				srcset={`/images/desktop/image-grid-2.jpg, /images/desktop/image-grid-2@2x.jpg 2x`}
				media="(min-width:1440px)"
				alt=""
			/>

			<source
				srcset={`/images/tablet/image-grid-2.jpg, /images/tablet/image-grid-2@2x.jpg 2x`}
				media="(min-width:768px)"
				alt=""
			/>

			<source
				srcset={`/images/mobile/image-grid-2.jpg, /images/mobile/image-grid-2@2x.jpg 2x`}
				media="(min-width:375px)"
				alt=""
			/>
			<img src="/images/mobile/image-grid-2.jpg" alt="" />
		</picture>
	</div>
	<div class="image-grid-3">
		<picture>
			<source
				srcset={`/images/desktop/image-grid-3.jpg, /images/desktop/image-grid-3@2x.jpg 2x`}
				media="(min-width:1440px)"
				alt=""
			/>

			<source
				srcset={`/images/tablet/image-grid-3.jpg, /images/tablet/image-grid-3@2x.jpg 2x`}
				media="(min-width:768px)"
				alt=""
			/>

			<source
				srcset={`/images/mobile/image-grid-3.jpg, /images/mobile/image-grid-3@2x.jpg 2x`}
				media="(min-width:375px)"
				alt=""
			/>
			<img src="/images/mobile/image-grid-3.jpg" alt="" />
		</picture>
	</div>
	<div class="be-inspired">
		<h2 class="heading-l">come & be inspired</h2>
		<p>We’re excited to welcome you to our gallery and see how our collections influence you.</p>
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

			picture img {
				object-fit: cover;
				object-position: center top;
			}
		}

		.image-grid-3 {
			grid-area: image-grid-3;
		}

		.be-inspired {
			grid-area: be-inspired;
			background-color: var(--color-almost-black);
			padding: 3rem 1.5rem 1.3rem 1.5rem;

			.heading-l {
				color: var(--color-white);
			}

			p {
				padding: 1.5rem 0;
				color: var(--color-white);
			}
		}

		@media (min-width: 768px) {
			padding: 7.5rem 2.5rem 7.2rem 2.5rem;
			grid-template-columns: [mosaic-left] 1fr [middle-col] 7.3rem [mosaic-right] 280px;
			grid-template-rows: [top] 1fr [middle-row] 313px [bottom] auto;
			grid-template-areas: unset;
			grid-row-gap: 0.8rem;

			.introduction {
				grid-column: mosaic-left;
				grid-row: top;
				padding-top: 2.3rem;
				padding-right: 4rem;

				h2 {
					padding-bottom: 1.5rem;
				}
			}

			.image-grid-1 {
				grid-column: middle-col / mosaic-right;
				grid-row: top;
				width: 398px;
			}

			.image-grid-2 {
				grid-column: mosaic-left / middle-col-end;
				grid-row: middle-row / bottom;
				width: 398px;
			}

			.image-grid-3 {
				grid-column: mosaic-right;
				grid-row: middle-row;
			}

			.be-inspired {
				grid-column: mosaic-right;
				grid-row: bottom;
				height: 396px;
				padding: 5rem 1.8rem 1.3rem 1.8rem;
			}
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
