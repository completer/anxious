<script lang="ts">
	import Video from '$lib/Video.svelte';
	import Image from '$lib/Image.svelte';
	const row1 = [
		{ name: 'followers-1million.mp4', kind: 'mp4', c: 'flex-1' },
		{ name: 'eat-me.mp4', kind: 'mp4', c: 'flex-[0.5]' },
		{ name: 'these-results-may-contain.webp', kind: 'img', c: 'flex-[1.5]' },
		{ name: 'suicide-frog.webp', kind: 'img', c: 'flex-1' },
		{ name: 'vr-headset-kid.mp4', kind: 'mp4', c: 'flex-1' },
		{ name: 'meme-happy-sad-face.webp', kind: 'img', c: 'flex-1' }
	];
</script>

<!-- <div class="w-full h-full">
	<div class="flex gap-1 h-[200px]">
		<div class="flex-1">
			<Video src="followers-1million.mp4" />
		</div>
		<div class="flex-[0.5]">
			<Video src="eat-me.mp4" />
		</div>
		<div class="flex-[1.5] object-fill">
			<img src="these-results-may-contain.webp" alt="" class="object-fill" />
		</div>
		<div class="flex-[0.8]">
			<img src="suicide-frog.webp" alt="" class="" />
		</div>
		<div class="flex-1">
			<Video src="vr-headset-kid.mp4" />
		</div>
		<div class="flex-1">
			<img src="meme-happy-sad-face.webp" alt="" class="" />
		</div>
	</div>
</div> -->

<!-- h-screen -->
<div class="w-full h-[400px]">
	<div
		class=" grid grid-cols-6 gap-1 h-full w-full"
		style="grid-template-rows: minmax(0, 1fr) minmax(0, 1fr);"
	>
		<!-- row 1 -->
		<div><Video src="followers-1million.mp4" class="object-cover h-full" /></div>
		<div><Video src="eat-me.mp4" class="object-cover h-full" /></div>
		<div><Image src="these-results-may-contain.webp" class=" w-full h-full" /></div>
		<div><Image src="suicide-frog.webp" class="object-cover h-full" /></div>
		<div><Video src="vr-headset-kid.mp4" class="object-cover h-full" /></div>

		<div><Image src="meme-happy-sad-face.webp" class="h-full" /></div>
	</div>

	<!-- row 2 -->
	<!-- <div class="row-span-2">
				<Video src="rainbow-tongue.mp4" class="w-full" />
			</div> -->
</div>

<style>
	.grid {
		grid-template-rows: 1fr 1fr;
	}
	.grid > div {
		overflow: hidden;
	}
</style>
