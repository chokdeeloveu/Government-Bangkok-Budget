<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>Display a map on a webpage</title>
<meta name="viewport" content="initial-scale=1,maximum-scale=1,user-scalable=no">
<link href="https://api.mapbox.com/mapbox-gl-js/v2.15.0/mapbox-gl.css" rel="stylesheet">
<script src="https://api.mapbox.com/mapbox-gl-js/v2.15.0/mapbox-gl.js"></script>
<style>
       body {
          margin:0;
          padding:0;
          font-family: sans-serif;
          font-size: 14px;
        }
        #map { position:absolute; top:0; bottom:0; width:100%; }
      li {
        padding: 3px 0;
      }
      #panel {
        background: white;
        width: 400px;
        border: 1px solid rgba(0, 0, 0, 0.05);
        position: absolute;
        right: 16px;
        top: 16px;
        box-shadow: 0 0 4px 0 rgba(0, 0, 0, 0.1);
        color: rgba(0, 0, 0, 0.5);
      }
      h4 {
        text-transform: uppercase;
        border-bottom: 1px solid rgba(0, 0, 0, 0.05);
        margin: 0;
        padding: 16px;
      }
      ul {
        list-style-type: none;
        margin: 0;
        padding: 16px;
      }
      ul span {
        width: 10px;
        height: 10px;
        display: inline-block;
        margin-right: 8px;
        border-radius: 50%;
      }
</style>
</head>
<body>
<div id="map"></div>
   <div id="panel" style="background: white; width: 400px; border 1px solid rgba(0, 0, 0, 0.05);">
  <h4>Government Budget Bangkok</h4>
  <ul>
    <li><span style="background: #f896ae;"></span>Budget Lower 250 MB</li>
    <li><span style="background: #ff5c69;"></span>Budget 251 - 300 MB</li>
    <li><span style="background: #fbcbdb;"></span>Budget 301 - 350 MB</li>
    <li><span style="background: #fc409b;"></span>Budget 351 - 400 MB</li>
    <li><span style="background: #fc409b;"></span>Budget 401 - 450 MB</li>
    <li><span style="background: #fc409b;"></span>Budget 451 - 500 MB</li>
    <li><span style="background: #fc409b;"></span>Budget 501 - 550 MB</li>
    <li><span style="background: #ff1a81;"></span>Budget 551 - 600 MB</li>
   </ul>
<script>
	mapboxgl.accessToken = 'pk.eyJ1IjoiY2hva2RlZWxvdmV1IiwiYSI6ImNsaW5tMjV3MTAwcHMzZ28xbmdtOGY1ZTQifQ.GqZoIa_oR0r-Gc14tx4h9w';
const map = new mapboxgl.Map({
container: 'map', // container ID
// Choose from Mapbox's core styles, or make your own style with Mapbox Studio
style: 'mapbox://styles/chokdeeloveu/clinm676x00nf01pg0q083qjw', // style URL
center: [100.515507, 13.729006],
  // starting position [lng, lat]
zoom: 10,
  minZoom: 10,
  maxZoom: 14,
  hash: false
});

  var nav = new mapboxgl.NavigationControl();
  map.addControl(nav, 'top-left');

  map.on('mousemove', function(event) {
    //console.log(event);
    if (map.loaded()) {
      var features = map.queryRenderedFeatures(event.point, {
        layers: ['map-bhq50q']
      });
      map.getCanvas().style.cursor = features.length ? 'pointer' : '';
    }
    /*
    if (features.length) {
      map.getCanvas().style.cursor = 'pointer';
    } else {
      map.getCanvas().style.cursor = '';
    }*/
  });

  map.on('click', function(event) {
  //console.log('Mouse clicked');
  //console.log(event.point);
  var geometry = event.point;
  var parameters = {
    layers: ['map-bhq50q']
  };
  var features = map.queryRenderedFeatures(geometry, parameters);
  //console.log(features);
  //console.log(features.length + ' features');
  var lot = features[0];
  console.log(map-bhq50q);

  if (features.length) {
    var fid = map-bhq50q.properties.fid || '—';
    var CHANGWAT_N = CHANGWAT_NNames[map-bhq50q.properties.CHANGWAT_N] || '—';
    var DISTRICT_N = map-bhq50q.properties.DISTRICT_N || '—';
    var SUBDISTR_1 = map-bhq50q.properties.SUBDISTR_1 || '—';
    var BUDGET = map-bhq50q.properties.BUDGET || '—';

    console.log(fid, CHANGWAT_N, DISTRICT_N, SUBDISTR_1, BUDGET);

    var popup = new mapboxgl.Popup()
      .setLngLat(event.lngLat)
      .setHTML('<dl>' +
        '<dt>fid</dt>' +
        '<dd>' + fid + '</dd>' +
        '<dt>CHANGWAT_N</dt>' +
        '<dd>' + CHANGWAT_N + '</dd>' +
        '<dt>DISTRICT_N</dt>' +
        '<dd>' + DISTRICT_N + '</dd>' +
        '<dt>SUBDISTR_1 Class</dt>' +
        '<dd>' + SUBDISTR_1 + '</dd>' +
        '<dt>BUDGET</dt>' +
        '<dd>' + BUDGET + '</dd>' +
      '</dl>')
      .addTo(map);
  }
});
  
  new mapboxgl.Popup()
.setLngLat([100.42189469999998, 13.671508299752707])
.setHTML("<h1>สำนักงานเขตบางบอน รวม 344,511,510 บาท</h1>")
.addTo(map);
  
    
  new mapboxgl.Popup()
.setLngLat([100.796705, 13.744336])
.setHTML("<h1>สำนักงานเขตลาดกระบัง รวม 588,620,400 บาท</h1>")
.addTo(map);
  
    new mapboxgl.Popup()
.setLngLat([100.655155, 13.903658])
.setHTML("<h1>สำนักงานเขตสายไหม รวม 377,451,700 บาท</h1>")
.addTo(map);
  
    
  new mapboxgl.Popup()
.setLngLat([100.615061, 13.674725])
.setHTML("<h1>สำนักงานเขตบางนา จำนวน 290,762,550 บาท</h1>")
.addTo(map);
  
    new mapboxgl.Popup()
.setLngLat([100.854907, 13.877399])
.setHTML("<h1>สำนักงานเขตหนองจอก จำนวน 591,923,050 บาท</h1>")
.addTo(map);
  
</script>
 
</body>
</html>