# Mapping_Earthquakes

## Earthquake Challenge

In this challenge, I created a map that displayed earthquake data in relation to the tectonic plates’ location on the earth, all the earthquakes with a magnitude greater than 4.5 on the map, and a third map option to toggle in between.

#### In the challenge_logic.js file you can find the code that creates the three map views here:
```
let streets = L.tileLayer('https://api.mapbox.com/styles/v1/mapbox/streets-v11/tiles/{z}/{x}/{y}?access_token={accessToken}', {
	attribution: 'Map data &copy; <a href="https://www.openstreetmap.org/">OpenStreetMap</a> contributors, <a href="https://creativecommons.org/licenses/by-sa/2.0/">CC-BY-SA</a>, Imagery (c) <a href="https://www.mapbox.com/">Mapbox</a>',
	maxZoom: 18,
	accessToken: API_KEY
});

let satelliteStreets = L.tileLayer('https://api.mapbox.com/styles/v1/mapbox/satellite-streets-v11/tiles/{z}/{x}/{y}?access_token={accessToken}', {
	attribution: 'Map data &copy; <a href="https://www.openstreetmap.org/">OpenStreetMap</a> contributors, <a href="https://creativecommons.org/licenses/by-sa/2.0/">CC-BY-SA</a>, Imagery (c) <a href="https://www.mapbox.com/">Mapbox</a>',
	maxZoom: 18,
	accessToken: API_KEY
});

let dark = L.tileLayer('https://api.mapbox.com/styles/v1/mapbox/dark-v10/tiles/{z}/{x}/{y}?access_token={accessToken}', {
	attribution: 'Map data &copy; <a href="https://www.openstreetmap.org/">OpenStreetMap</a> contributors, <a href="https://creativecommons.org/licenses/by-sa/2.0/">CC-BY-SA</a>, Imagery (c) <a href="https://www.mapbox.com/">Mapbox</a>',
	maxZoom: 18,
	accessToken: API_KEY
});
```
#### Also in the challenge_logic.js file you will find the layer groups created to display earthquake data over the past week, major earthquakes and tectonic plates:
```
let allEarthquake = new L.LayerGroup();
let tectonicPlates = new L.LayerGroup();
let majorEarthquake = new L.LayerGroup();
```

## Using the map
In the upper right hand corner of the map webpage is where you can toggle between the three different map view options; satellite, streets and dark. You can also toggle between the three sets of data that was pulled in using d3.json.
