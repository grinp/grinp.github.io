<!DOCTYPE html>
<html>
<head>
	
    <!--Add a title below-->
	<title>Places suitable for Fitness Club in Rochester</title>

    <!--Add a comment here explaining what we are doing in next three lines-->
      <!--I think the first line calls to style file of leaflet map, the second line opens leaflet map itself and the third line opens geojson file with objects.-->
	<link rel="stylesheet" href="leaflet/leaflet.css"/>
    <script src="leaflet/leaflet.js"></script>
    <script src="RochesterBoundaries.geojson"></script> 
    <script src="SuitabilityByBuildings.geojson"></script>
    <script src="SuitabilityByTract.geojson"></script>
    
    <style>
		html, body {
			height: 100%;
			margin: 0;
            }
            
        #map{
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }
        
    
		.info {
			padding: 6px 8px;
			font: 14px/16px Arial, Helvetica, sans-serif;
			background: white;
			background: rgba(255,255,255,0.8);
			box-shadow: 0 0 15px rgba(0,0,0,0.2);
			border-radius: 5px;
		}
		.info h4 {
			margin: 0 0 5px;
			color: #777;
		}
		
		}
		.info h6 {
			margin: 0 0 10px;
			color: #000000;
		}

		.legend {
			text-align: left;
			line-height: 18px;
			color: #555;
		}
		.legend i {
			width: 18px;
			height: 18px;
			float: left;
			margin-right: 8px;
			opacity: 0.7;
		}
    </style>
	
</head>
<body>
<!--This is the div element where the map will go, it is given the id="map" which will be referenced below-->
<div id="map"></div>

<script>
	
	   <!--Add a comment here -->
    <!--Lines below escribe which  stile of the map we want to use. As I understand we are goin to use Stamen design and creativecommos. for map data we are going to use openstreet map. We make max zoom as 20 and min zoom as 0.   -->
    
	var basemap = L.tileLayer('https://{s}.basemaps.cartocdn.com/light_all/{z}/{x}/{y}{r}.png', {
	      attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors &copy; <a href="https://carto.com/attributions">CARTO</a>',
	      subdomains: 'abcd',
	      maxZoom: 19
    }); 
    
	
	//here we actually add the  geoJson SuitabilityByTract file and set the style but calling the style function
    // and calling the onEachFeature function to handle dynamic events (hover or mouseover, click, mouseout) 
	var SuitabilityByTract = L.geoJson(SuitabilityByTract, {style: style,  onEachFeature: onEachFeature});
	
	// this is a function to setting up the color scheme the CBG geojson layer in the map will use, using kind of an orange to red 
    //this function gets called below 
    //you ccould change to a different system
	
  	function style(feature) {
      return {
        fillColor: getColor(feature.properties.MEAN),
        weight: 0,
        opacity: 1,
        fillOpacity: 0.7
      };
    }
    
    // this is a function to setting up the color scheme the CBG geojson layer in the map will use, using kind of an orange to red 
    //this function gets called below 
    //you ccould change to a different system
	function getColor(d) {
		return  d > 18.51 ?	 '#00ff2f':	
		        d > 18.10 ?  '#eeff00':
				d > 16.94 ?  '#ff9500':
				d > 15.56 ?  '#ff5100':
						   '#ff0000';
	}	
        
    //here we actually add the SuitabilityByBuildings geojson file and set the style but calling the style function
    // and calling the onEachFeature function to handle dynamic events (hover or mouseover, click, mouseout) 
	var SuitabilityByBuildings = L.geoJson(SuitabilityByBuildings, {style: style2, onEachFeature: onEachFeature2});
	
	function style2(feature) {
      return {
        fillColor: getColor2(feature.properties.gridcode),
        weight: 0.4,
        opacity: 1,
        fillOpacity: 1
      };
    }
		
// this is a function to setting up the color scheme the CBG geojson layer in the map will use, using kind of an orange to red 
    //this function gets called below 
    //you ccould change to a different system
	function getColor2(d) {
		return  d > 19 ?  '#00ff2f' :
				d > 18 ?  '#eeff00' :
				d > 17 ?  '#ff9500' :
				d > 0  ?  '#ff5100' :
						'#ff0000';
	}	
		
	var boundaries = L.geoJSON(RochesterBoundaries, {
          style: {
            color: "#706f6e",
            weight: 0.7,
            fillOpacity: 0.0
            
        }
    })
    
    
    <!--Here we are going to open our map with central coordinates 42.0667, -93.4 and with zoom level 9 -->
	var map = L.map('map', {
		  center: [44.024411, -92.472319],
          zoom: 11,
          layers: [ basemap, boundaries, SuitabilityByTract, SuitabilityByBuildings],
         
     });

    var overlays = {
          "Tracts": SuitabilityByTract,
          "Buildings": SuitabilityByBuildings,
          "Boundaries": boundaries
     };
    L.control.layers(null,overlays).addTo(map);

        // create a control which will go in a div element and will display information from the GeoJson files
	var info = L.control();

    //create the div element, doing this through JavaScript, could have done differently (HTML)
	info.onAdd = function(map) {
		this._div = L.DomUtil.create('div', 'info');
		this.update();
		return this._div;
	};

    //where we set up the information that will be presented in the info window in the uppper right
    //the props are the attributes being read from the CBG geojson 
	info.update = function(props) {
	  
		this._div.innerHTML = '<h4>Suitability model for a fitness club from Cedar Falls</h4>' + 
		'<p> The results were obtained on the basis of competitor locations, <br> socio-demographic data, as well as proximity to restaurants and cafes</p>' +
		  (props ? '<br/>' + props.NAMELSAD +  '<br/><br/>' +
            props.MEAN + ' points by suitability model<br/><br/>' +
            props.gridcode + ' points by suitability model for building<br/><br/>'
			: 'Hover over a Tract');
	};	info.addTo(map);
 	
    
     
 
    

    //this function is the code that gets called from below when user hovers on polygon
    //it changes sytling of the polygon hovered on and then updates the info element in the upper right
	function highlightFeature(e) {
		var layer = e.target;

		layer.setStyle({
			weight: 5,
			color: '#666',
			dashArray: '',
			fillOpacity: 0.7
		});

		if (!L.Browser.ie && !L.Browser.opera && !L.Browser.edge) {
			layer.bringToFront();
		}

		info.update(layer.feature.properties);
	}

    //resets the polygon symbology after user moves cursor off the polygon
	function resetHighlight(e) {
		SuitabilityByTract.resetStyle(e.target);
		info.update();
	}

    //resets the polygon symbology after user moves cursor off the polygon
	function resetHighlight2(e) {
		SuitabilityByBuildings.resetStyle(e.target);
		info.update();
	}
    //onEachFeature is a leaflet function where we indicate what we want to do on certain events
    //in this case, we call two specific functions for when mouseover (change stying to highlight polygon hovered over)
    //or mouseout (reset styling for polygon) events happen
	function onEachFeature(feature, layer) {
		layer.on({
			mouseover: highlightFeature,
			mouseout: resetHighlight,

		});
	}

   function onEachFeature2(feature, layer) {
		layer.on({
			mouseover: highlightFeature,
			mouseout: resetHighlight2,

		});
	}

//  Legend

    var legend = L.control({position: 'bottomright'});
    legend.onAdd = function (map) {

    var div = L.DomUtil.create('div', 'info legend');
        grades = [19, 18, 17, 0],
        labels = ['<strong>Suitability</strong>'],
        categories = ['High','Medium','Medium-Low','Low'];

    for (var i = 0; i < grades.length; i++) {

            div.innerHTML += 
            labels.push(
                '<i style="background:' + getColor(grades[i]+0.5) + '"></i> ' +
            (categories[i] ? categories[i] : '+'));

        }
        div.innerHTML = labels.join('<br>');
    return div;
    };
    legend.addTo(map);

</script>

</body>
</html>
