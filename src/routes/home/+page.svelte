<script>
	import { resolve } from '$app/paths';
	import SwiperCategory from '$lib/SwiperCategory.svelte';

	const categories = [
		{
			href: 'category/living-room',
			icon: 'assets/images/icons/living-rooms.svg',
			title: 'Living Room',
			count: 1_353
		},
		{
			href: 'category/security',
			icon: 'assets/images/icons/security.svg',
			title: 'Security',
			count: 982
		},
		{
			href: resolve('category/kitchen'),
			icon: 'assets/images/icons/kitchen.svg',
			title: 'Kitchen',
			count: 1_120
		},
		{
			href: 'category/storage',
			icon: 'assets/images/icons/storage.svg',
			title: 'Storage',
			count: 745
		}
		// tambah lagi …
	];
</script>

<div id="background" class="absolute left-0 right-0 top-0">
	<img
		src="assets/images/backgrounds/banner.png"
		alt="background"
		class="h-[349.02px] w-full object-cover object-bottom"
	/>
</div>
<section id="navtop" class="fixed left-0 right-0 top-5 z-30">
	<div class="mx-auto max-w-160 px-5">
		<div class="flex items-center justify-between rounded-2xl bg-white px-4 py-3.5">
			<a href="#" class="shrink-0">
				<img src="assets/images/logos/suija-logo.svg" alt="sujia-logo" />
			</a>
			<ul class="flex items-center gap-2.5">
				<li class="shrink-0">
					<a href="#">
						<div
							class="flex h-11 w-11 shrink-0 item-centered justify-center rounded-full border border-shujia-graylight"
						>
							<img src="assets/images/icons/bell.svg" alt="notifications" />
						</div>
					</a>
				</li>
				<li class="shrink-0">
					<a href="#">
						<div
							class="flex h-11 w-11 shrink-0 item-centered justify-center rounded-full border border-shujia-graylight"
						>
							<img src="assets/images/icons/basket.svg" alt="shoping-cart" />
						</div>
					</a>
				</li>
			</ul>
		</div>
	</div>
</section>
<header class="relative ml-5 mt-32 w-61.5">
	<h1 class="text-3xl font-extrabold leading-12">Discover Top Home Services</h1>
</header>
<div id="container" class="flex flex-col gap-7.5">
	<section id="categories" class="swiper w-full overflow-x-hidden">
		<SwiperCategory items={categories} />
	</section>
	<section id="adverticement"></section>
	<section id="popularsummer"></section>
</div>
<nav id="navbuttom"></nav>
