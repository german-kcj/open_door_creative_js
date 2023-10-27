# Leaflet - Mappa - p5js

<figure><img src="../.gitbook/assets/Screen Shot 2023-10-25 at 8.34.55 PM.png" alt=""><figcaption></figcaption></figure>

```javascript

// Options for map
let options = {
  lat: 0,
  lng: 0,
  zoom: 2,
  style: 'http://{s}.tile.osm.org/{z}/{x}/{y}.png'
}

// Create an instance of Leaflet
let mappa = new Mappa('Leaflet');
let myMap;

let canvas;
let countries;

function preload(){
  // Load the data
    countries = loadTable('/data/world_pop.csv', 'csv', 'header');
}

function setup() {
  canvas = createCanvas(800, 700);

  // Create a tile map and overlay the canvas on top.
  myMap = mappa.tileMap(options);
  myMap.overlay(canvas);

  fill(70, 203,31);	
  stroke(100);
}

function draw() {
  drawPopulation()
}

function drawPopulation() {
  // Clear the canvas
  clear();
  

  for (let i = 0; i < countries.getRowCount(); i++) {
    // Get the lat/lng of each country 
    let latitude = Number(countries.getString(i, 'latitude'));
    let longitude = Number(countries.getString(i, 'longitude'));
    let name = countries.getString(i, 'Country/Territory');
    let pop = countries.getString(i, '2022 Population');

    // Only draw them if the position is inside the current map bounds. We use a
    // Leaflet method to check if the lat and lng are contained inside the current
    // map. This way we draw just what we are going to see and not everything. See
    // getBounds() in http://leafletjs.com/reference-1.1.0.html
    if (myMap.map.getBounds().contains({lat: latitude, lng: longitude})) {
      
      // Transform lat/lng to pixel position
      let pos = myMap.latLngToPixel(latitude, longitude);
      console.log(pos)
      
      // Get the size of the population and map it.
      let size = countries.getString(i, '2022 Population');
      
      size = map(size, 510, 1425887337, 2, 50) + myMap.zoom();
      
      fill(250,0,250)
      ellipse(pos.x, pos.y, size, size);
      let d = dist(pos.x, pos.y, mouseX, mouseY);
      if(d < 5){
        let num = new Intl.NumberFormat('en-IN', { maximumSignificantDigits: 3 }).format(pop);
        stroke(0);
        fill(0);
        text(name, pos.x+10, pos.y);
        text(num, pos.x+10, pos.y+20);
        
      }
    }
  }
}

```

### p5js Link

{% embed url="https://editor.p5js.org/Garcila/sketches/yOWjPW5fG" %}
