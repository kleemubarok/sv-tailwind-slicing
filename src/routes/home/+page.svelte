<script>
	import { resolve } from '$app/paths';
	import SwiperCategory from '$lib/SwiperCategory.svelte';
	import PopularThisSummer from '$lib/SwiperPopularThisSummer.svelte';

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

	const popular_items = [
		{
			href: resolve('category/kitchen'),
			rating: '4.8',
			img: 'https://picsum.photos/id/1/200/300',
			title: 'Home Family Theater Best Lights Installation',
			room_name: 'Living Room',
			time: '15 Hours',
			price: 'Rp 8.560.392'
		},
		{
			href: resolve('category/kitchen'),
			rating: '4.8',
			img: 'https://picsum.photos/id/20/200/300',
			title: 'Rumah Kaca',
			room_name: 'Garden ',
			time: '15 Hours',
			price: 'Rp 6.560.392'
		}
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
	<section id="adverticement" class="px-5">
		<a href="#">
			<img src="assets/images/backgrounds/ads.png" alt="icon" />
		</a>
	</section>
	<section id="popularsummer" class="space-y-3.5">
		<h2 class="pl-5 tex-xl font-bold leading-7">Popular This Summer</h2>
		<div id="PopularSummerSlider" class="px-5 swiper w-full overflow-x-hidden">
			<PopularThisSummer items={popular_items} />
		</div>
	</section>
</div>
<nav id="navbuttom" class="fixed bottom-5 left-0 right-0 z-30 mx-auto w-full">
	<div class="mx-auto max-w-160 px-5">
		<div class="rounded-3xl bg-shujia-black px-5 py-3.5">
			<ul class="flex items-center gap-[20.30px]">
				<li class="w-full">
					<a href="#">
						<div
							class="flex items-center justify-center gap-2 rounded-full bg-shujia-orange px-[18px] py-[10px] transition-all duration-300 hover:shadow-[0px_4px_10px_0px_#D04B1E80]"
						>
							<img
								class="h-6 w-6 shrink-0"
								src="assets/images/icons/calendar-gemini.svg"
								alt="icon"
							/>
							<p class="text-sm font-semibold leading-[21px] text-white">Browse</p>
						</div>
					</a>
				</li>
				<li class="shrink-0">
					<a href="#">
						<div
							class="flex h-[44px] w-[44px] shrink-0 items-center justify-center rounded-full border border-shujia-graylight transition-all duration-300 hover:border-shujia-orange"
						>
							<img src="assets/images/icons/toilet-paper.svg" alt="icon" />
						</div>
					</a>
				</li>
				<li class="shrink-0">
					<a href="#">
						<div
							class="flex h-[44px] w-[44px] shrink-0 items-center justify-center rounded-full border border-shujia-graylight transition-all duration-300 hover:border-shujia-orange"
						>
							<img src="assets/images/icons/chat.svg" alt="icon" />
						</div>
					</a>
				</li>
				<li class="shrink-0">
					<a href="#">
						<div
							class="flex h-[44px] w-[44px] shrink-0 items-center justify-center rounded-full border border-shujia-graylight transition-all duration-300 hover:border-shujia-orange"
						>
							<img src="assets/images/icons/profile.svg" alt="icon" />
						</div>
					</a>
				</li>
			</ul>
		</div>
	</div>
</nav>
