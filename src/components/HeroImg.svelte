<script>
	import imageHeroMobile from '@/assets/mobile/image-hero.jpg'
	import imageHeroMobile2x from '@/assets/mobile/image-hero@2x.jpg'
	import imageHeroTablet from '@/assets/tablet/image-hero.jpg'
	import imageHeroTablet2x from '@/assets/tablet/image-hero@2x.jpg'
	import imageHeroDesktop from '@/assets/desktop/image-hero.jpg'
	import imageHeroDesktop2x from '@/assets/desktop/image-hero@2x.jpg'
</script>

<picture>
	<source
		srcset={`${imageHeroDesktop}, ${imageHeroDesktop2x} 2x`}
		media="(min-width:1440px)"
		alt=""
	/>

	<source srcset={`${imageHeroTablet}, ${imageHeroTablet2x} 2x`} media="(min-width:768px)" alt="" />

	<source srcset={`${imageHeroMobile}, ${imageHeroMobile2x} 2x`} media="(min-width:375px)" alt="" />
	<img src={imageHeroMobile} alt="" />
</picture>
