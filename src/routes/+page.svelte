<script>
	import HomeFooter from '@/components/home/HomeFooter.svelte'
	import HomeHeader from '@/components/home/HomeHeader.svelte'
	import HomeMain from '@/components/home/HomeMain.svelte'
</script>

<div class="container">
	<HomeHeader />
	<HomeMain />
</div>

<HomeFooter />

<style lang="scss">
	.container {
		margin-inline: auto;
		max-width: 375px;

		@media (min-width: 768px) {
			max-width: 768px;
		}

		@media (min-width: 1440px) {
			max-width: 1440px;
		}
	}
</style>
