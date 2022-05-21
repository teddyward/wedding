<div class="page-title durham-page-title">
    <div>Things to do in Durham</div>
    <div class="page-subtitle">Zoom in for descriptions</div>
</div>
<div id="map"></div>
<div class="external-guides">
    <div>In addition, you can check out the following resources:</div>
    <div><a href="https://www.vogue.com/article/durham-travel-guide-north-carolinas-hippest-city"><i>Why Durham is North Carolina's Hippest City</i></a> in Vogue</div>
    <div><a href="https://www.alltrails.com/us/north-carolina/durham">AllTrails guide to Durham</a></div>
</div>

<script>
    import { onMount } from 'svelte';

    onMount(() => {
        mapboxgl.accessToken = 'pk.eyJ1IjoidGhyb3dhd2F5ODY3NTMwOSIsImEiOiJja2Q3bmZ4c2ExZWw0MnlvMmZ2OWR1MHE5In0.lt1pIT7P5njAWbfnucdQmQ';

        const map = new mapboxgl.Map({
            container: 'map', // container id
            style: 'mapbox://styles/throwaway8675309/cku1unoy72a8318o6irmyf83v', // style URL
            center: [-78.91618516143913, 36.020195587756106], // starting position [lng, lat]
            zoom: 11.09 // starting zoom
        });
        map.on('zoomend', () => alert(map.getZoom()))
        setTimeout(() => map.resize(), 1000)
    });
</script>

<style>
    #map {
        height: 75%;
        margin-top: 20px;
        margin-bottom: 20px;
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

    .external-guides {
        display: flex;
        height: 20%;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
    }
</style>
