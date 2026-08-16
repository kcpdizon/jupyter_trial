---
Title: introduction
--- 

This project documents the present-day cultural landscape of Davao City's Chinatown, also known as Santa Ana or Uyanguren, analyzing its spatial characteristics and built environment.

<!-- 1. MapLibre CSS -->
<link rel="stylesheet" href="https://unpkg.com/maplibre-gl@6.3.0/dist/maplibre-gl.css" />

<!-- 2. Map Container & Fly Button -->
<div style="position: relative; width: 100%; height: 450px; margin: 20px 0; border-radius: 8px; overflow: hidden;">
    <div id="map" style="width: 100%; height: 100%;"></div>
    <button id="fly" style="position: absolute; top: 15px; left: 15px; z-index: 10; padding: 10px 16px; background: #ee8a65; color: white; border: none; border-radius: 4px; font-weight: bold; cursor: pointer;">
        Fly to Davao
    </button>
</div>

<!-- 3. Map Script -->
<script type="module">
    import * as maplibregl from 'https://unpkg.com/maplibre-gl@6.3.0/dist/maplibre-gl.mjs';

    const map = new maplibregl.Map({
        container: 'map',
        style: 'https://tiles.openfreemap.org/styles/bright',
        center: [122.5, 12.8], // Default: Philippines
        zoom: 5.5
    });

    document.getElementById('fly').addEventListener('click', () => {
        map.flyTo({
            center: [125.597816, 7.065629], // Target: Davao
            zoom: 13,
            essential: true
        });
    });
</script>
