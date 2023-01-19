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

<style lang="scss">
	picture img {
		object-fit: cover;
	}
</style>
