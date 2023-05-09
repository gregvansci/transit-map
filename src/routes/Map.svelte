<script>
  import { onMount } from 'svelte';
  import mapboxgl from 'mapbox-gl';
  import { PUBLIC_MAPBOX_ACCESS_TOKEN } from '$env/static/public';

  let map;
	const token = PUBLIC_MAPBOX_ACCESS_TOKEN;
  onMount(() => {
		mapboxgl.accessToken = token;
		map = new mapboxgl.Map({
			container: 'map',
			style: 'mapbox://styles/mapbox/streets-v11',
			center: [-118.25, 33.95],
			zoom: 9.5
		})
	})
</script>

<div class="" id="map"></div>