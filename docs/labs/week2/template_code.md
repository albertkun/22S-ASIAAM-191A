# Final Template Code

```html title="index.html" linenums="1"
<!DOCTYPE html>
<html>
    <head>
        <title>Hello World with Leaflet</title>
        <meta charset="utf-8" />
        <link rel="shortcut icon" href="#">
        <!-- I'd add some style if here if I had any -->
        <link rel="stylesheet" href="styles/style.css">
        <script>
            console.log('Hello Asian Am 191! :)')
        </script>
        <!-- Leaflet's css-->
        <link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css" />
    </head>
    
    <body>
        <header>
            My Map
        </header>
        
        <div class="main">
            
        </div>
        <div id="map"></div>
        <div id="footer">
            Copyright(2022)
        </div>

    </body>
</html>
```

```js title="/js/init.js" linenums="1"
const map = L.map('map').setView([34.0709, -118.444], 5);

// Leaflet tile layer, i.e. the base map
L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
	attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
}).addTo(map);

//JavaScript let variable declaration to create a marker
let marker = L.marker([34.0709, -118.444]).addTo(map)
		.bindPopup('Math Sciences 4328 aka the Technology Sandbox<br> is the lab where I work in ')
		// .openPopup();
        
fetch("map.geojson")
	.then(response => {
		return response.json();
		})
    .then(data =>{
        // Basic Leaflet method to add GeoJSON data
            // the leaflet method for adding a geojson
            L.geoJSON(data, {
                pointToLayer: function (feature, latlng) {
                    return L.circleMarker(latlng, {color: feature.properties.color});
                }
            }).bindPopup(function (layer) {
                return layer.feature.properties.place;
            }).addTo(map);
        });

```

```css title="/styles/style.css" linenums="1"

body{
    display: grid;
    grid-template-columns: 1fr; 
    grid-auto-rows: minmax(5px, auto);
    grid-template-areas: "header" "main_content" "footer";
    height: 100vh;
}

header{
    grid-area: header;
}

#footer{
    grid-area: footer;
}

.main{
    display: grid;
    grid-area: main_content;
    grid-template-areas: "mappanel" "content";
}

#map{
    height:80vh;
    grid-area: mappanel;
}

#contents{
    grid-area: content;
}


```

Now you should be ready to take on the [lab assignment](lab_assignment.md)!