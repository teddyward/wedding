<div class="page-title durham-page-title">
    <div>Things to do in Durham</div>
    <div class="page-subtitle">Zoom in for descriptions</div>
</div>
<div id="map"></div>

<script>
    import { onMount } from 'svelte';

    onMount(() => {
        mapboxgl.accessToken = 'pk.eyJ1IjoidGhyb3dhd2F5ODY3NTMwOSIsImEiOiJja2Q3bmZ4c2ExZWw0MnlvMmZ2OWR1MHE5In0.lt1pIT7P5njAWbfnucdQmQ';

        const map = new mapboxgl.Map({
            container: 'map', // container id
            style: 'mapbox://styles/throwaway8675309/cku1unoy72a8318o6irmyf83v', // style URL
            center: [-78.90581, 36.00548], // starting position [lng, lat]
            zoom: 12.32 // starting zoom
        });
    });
</script>

<style>
    #map {
        height: 100%;
        margin-top: 20px;
        min-width: 90%;
        width: 90%;
    }
    .durham-page-title {
        align-items: center;
        flex-direction: column;
    }

    .page-subtitle {
        font-size: 12px;
        font-style: italic;
    }
</style>
