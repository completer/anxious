<script lang="ts">
	export let src: string;
	let cls: string = '';
	export { cls as class };
</script>

<img {src} class={cls} alt="" />
