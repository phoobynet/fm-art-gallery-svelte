<script lang="ts">
	type Direction = 'left' | 'right'
	export let direction: Direction
	export let href: string
</script>

<a class="link-button" class:right={direction === 'right'} class:left={direction === 'left'} {href}>
	<div class="content">
		<slot />
	</div>
	<div class="arrow">
		{#if direction === 'right'}
			<img src="/images/icon-arrow-right.svg" alt="" />
		{:else}
			<img src="/images/icon-arrow-left.svg" alt="" />
		{/if}
	</div>
</a>

<style lang="scss">
	.link-button {
		display: grid;
		align-items: center;
		justify-content: space-between;
		grid-template-rows: 1fr;
		height: 72px;
		text-decoration: none;

		.content {
			display: flex;
			align-items: center;
			justify-content: center;
			text-transform: uppercase;
			font-family: var(--ff-big-shoulders-display);
			font-weight: var(--fw-black);
			background-color: var(--color-almost-black);
			color: var(--color-white);
			font-size: 20px;
			letter-spacing: 3.64px;
			height: 100%;
		}

		.arrow {
			display: flex;
			align-items: center;
			justify-content: center;
			place-self: stretch;
			width: 56px;
			background-color: var(--color-gold);

			img {
				width: 11px;
				height: 28px;
			}
		}

		&:hover {
			.content {
				background-color: var(--color-gold);
				color: var(--color-almost-black);
				transition: 0.5s;
			}

			.arrow {
				background-color: var(--color-almost-black);
				color: var(--color-gold);
				transition: 0.5s;
			}
		}

		&.right {
			grid-template-columns: 1fr auto;

			.content {
				grid-column: 1;
			}

			.arrow {
				grid-column: 2;
			}
		}

		&.left {
			grid-template-columns: auto 1fr;

			.content {
				grid-row: 1;
				grid-column: 2;
			}

			.arrow {
				grid-row: 1;
				grid-column: 1;
			}
		}
	}
</style>
