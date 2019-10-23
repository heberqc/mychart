<script>
	export let name
	import { onMount } from 'svelte'
	import Highcharts from 'highcharts'


	onMount(async () => {
		// Apply the theme
		Highcharts.setOptions(myChartsTheme)
		// Add the data
		const myChart = Highcharts.chart('container', {
			chart: {
				type: 'bar',
			},
			title: {
				text: 'Fruit Consumption',
			},
			xAxis: {
				categories: ['Apples', 'Bananas', 'Oranges'],
			},
			yAxis: {
				title: {
					text: 'Fruit eaten',
				},
			},
			series: [
				{
					name: 'Jane',
					data: [1, 0, 4],
				},
				{
					name: 'John',
					data: [5, 7, 3],
				},
			],
		})
	})
</script>

<style>
	h1 {
		color: red;
	}
</style>

<h1>Hello {name}!</h1>

<div id="container" style="widht:100%;height:400px;"></div>
