<script>
	/* Swiper 11 + Svelte 5 */
	import { register } from 'swiper/element/bundle'; // web-component
	import { resolve } from '$app/paths';
	register(); // daftarkan <swiper-container>

	// props
	let { items = [], class: klass = '' } = $props();
</script>

<swiper-container
	class="swiper-wrapper {klass}"
	slides-per-view="auto"
	space-between="20"
	slidesOffsetAfter="20"
	slidesOffsetBefore="20"
>
	{#each items as cat (cat.id)}
		<swiper-slide class="w-fit!">
			<a href={resolve(cat.href)} class="card">
				<div
					class="shrink-0 space-y-3 rounded-3xl border
                 border-shujia-graylight bg-white py-4 text-center
                 transition-all duration-300 hover:border-shujia-orange"
				>
					<div
						class="mx-auto flex h-17.5 w-17.5 shrink-0
                   items-center justify-center overflow-hidden
                   rounded-full"
					>
						<img src={cat.icon} alt={cat.title} class="h-full w-full object-cover" />
					</div>
					<div class="flex min-w-32.5 flex-col gap-0.5">
						<h3 class="font-semibold">{cat.title}</h3>
						<p class="text-sm leading-5.25 text-shujia-gray">
							{cat.count.toLocaleString()} Services
						</p>
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
