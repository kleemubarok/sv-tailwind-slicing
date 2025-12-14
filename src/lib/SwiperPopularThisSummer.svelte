<script>
	/* Swiper 11 + Svelte 5 */
	import { register } from 'swiper/element/bundle'; // web-component
	import { resolve } from '$app/paths';
	register(); // daftarkan <swiper-container>

	// props
	let { items = [], class: klass = '' } = $props();
</script>

<swiper-container class="swiper-wrapper {klass}" slides-per-view="auto" space-between="20">
	{#each items as item (item.id)}
		<swiper-slide class="w-fit!">
			<a href={resolve(item.href)} class="card">
				<div
					class="relative flex w-58 shrink-0 flex-col gap-3 overflow-hidden rounded-3xl border border-shujia-graylight bg-white p-4 transition-all duration-300 hover:border-shujia-orange"
				>
					<span class="absolute right-6.5 top-6.5 shrink-0 rounded-full bg-white px-2 py-1.75">
						<div class="flex items-center gap-0.5">
							<img src="assets/images/icons/star-rating.svg" alt="star-rating" />
							<p class="text-xs font-semibold leading-4.5">{item.rating}</p>
						</div>
					</span>
					<div
						class="flex h-35 w-full shrink-0 items-center justify-center overflow-hidden rounded-2xl bg-[#D9D9D9]"
					>
						<img src={item.img} alt="Popular Items" />
					</div>
					<h3 class="line-clamp-2 min-h-[48px] font-semibold">{item.title}</h3>
					<div class="flex flex-col gap-y-3">
						<div class="flex items-center gap-2">
							<img
								class="h-5 w-5 shrink-0"
								src="assets/images/icons/calendar.svg"
								alt="romm name icon"
							/>
							<p class="text-sm leading-5.25 text-shujia-gray">{item.room_name}</p>
						</div>
						<div class="flex items-center gap-2">
							<img class="h-5 w-5 shrink-0" src="assets/images/icons/clock.svg" alt="time icon" />
							<p class="text-sm leading-5.25 text-shujia-gray">{item.time}</p>
						</div>
						<strong class="font-semibold text-shujia-orange">{item.price}</strong>
						<img
							class="absolute bottom-0 right-0"
							src="assets/images/backgrounds/crown.svg"
							alt="crown icon"
						/>
					</div>
				</div>
			</a>
		</swiper-slide>
	{/each}
</swiper-container>

<style>
	/* tambahan kecil bila perlu */
	swiper-container::part(container) {
		padding-bottom: 4px; /* agar shadow tidak terpotong */
	}
</style>
