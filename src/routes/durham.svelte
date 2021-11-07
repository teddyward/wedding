<div class="page-title">
    <div>What to do in Durham</div>
</div>
<div id="map"></div>

<script>
    import { onMount } from 'svelte';

    onMount(() => {
        mapboxgl.accessToken = 'pk.eyJ1IjoidGhyb3dhd2F5ODY3NTMwOSIsImEiOiJja2Q3bmZ4c2ExZWw0MnlvMmZ2OWR1MHE5In0.lt1pIT7P5njAWbfnucdQmQ';

        var map = new mapboxgl.Map({
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
        width: 100%;
    }
</style>
