<script lang="ts">
	import { onMount } from 'svelte';
	import Chart from 'chart.js/auto';

	import Papa from 'papaparse';
	import csv from '$lib/data/depressive-girls.csv?raw';

	let canvas: HTMLCanvasElement;

	const parsed = Papa.parse(csv, { header: true, dynamicTyping: true, skipEmptyLines: true });
	const labels = parsed.data.map((row: any) => row['Year']);
	const girls = parsed.data.map((row: any) => row['Girls']);

	onMount(() => {
		const ctx = canvas.getContext('2d');
		if (!ctx) throw new Error('Could not get 2d context');

		new Chart(ctx, {
			type: 'line',
			data: {
				labels: labels,
				datasets: [{ label: 'Girls', data: girls }]
			},
			options: {
				scales: {
					x: {
						display: true,
						title: { display: true, text: 'Year' }
					},
					y: {
						display: true,
						title: { display: true, text: 'Numbers' },
						min: 0
					}
				}
			}
		});
	});
</script>

<div class="">
	<canvas bind:this={canvas} class="" />
</div>
