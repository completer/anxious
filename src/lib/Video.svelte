<script lang="ts">
	export let src: string;
	let cls: string = '';
	export { cls as class };
</script>

<video autoplay loop muted class={cls}>
	<source {src} type="video/mp4" />
	<track kind="captions" />
</video>
