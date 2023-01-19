<footer>
	<img src="/images/logo-light.svg" alt="" class="logo" />
	<p>
		The Modern Art Gallery is free to all visitors and open seven days a week from 8am to 9pm. Find
		us at 99 King Street, Newport, USA.
	</p>
	<div class="social-media">
		<img src="/images/icon-facebook.svg" alt="facebook" />
		<img src="/images/icon-instagram.svg" alt="instagram" />
		<img src="/images/icon-twitter.svg" alt="twitter" />
	</div>
</footer>

<style lang="scss">
	footer {
		background-color: var(--color-almost-black);
		padding: 3rem 2rem;
		margin-top: 7.5rem;
		width: 100%;

		.logo {
			width: 110px;
			height: 40px;
		}

		p {
			color: var(--color-white);
			font-size: var(--fs-small);
			line-height: var(--lh-small);
			padding: 2.37rem 0;
		}

		.social-media {
			display: flex;
			gap: 1.5rem;
			img {
				width: 20px;
				height: 20px;
			}
		}

		@media (min-width: 768px) {
			height: 216px;
			margin-top: 0;
			padding: 3.5rem 2.5rem;
			display: flex;
			width: 100%;
			justify-content: space-between;
			align-items: start;

			p {
				padding: 0;
				max-width: 281px;
			}
		}
	}
</style>
