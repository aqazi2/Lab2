<!DOCTYPE html>
<html>
    <head>
        <title>Lab 2</title>

         <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css"
           integrity="sha256-p4NxAoJBhIIN+hmNHrzRCf9tD/miZyoHS5obTRR9BMY="
           crossorigin=""/>

         <script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"
           integrity="sha256-20nQCchB9co0qIjJZRGuk2/Z9VM+kNiyxNV1lvTlZBo="
           crossorigin=""></script>

    </head>

    <body>
        <div id="map" style="height: 500px"></div>

        <script type="text/javascript">

          var map = L.map('map', {
              center: [38.16, -96.96],
              zoom: 4
          });

          L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
               attribution: '@ <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors',
               maxZoom: 4,
               minZoom: 4
            }).addTo(map);
					 var timeIcon = L.icon({
              iconUrl: 'time.png', // url that links to the icon image file
              iconSize:     [38, 38], // size of the icon image in pixels
              iconAnchor:   [19, 19], // the top left corner of the icon will be aligned so that this point is at the marker's geographical location
              popupAnchor:  [0, -10] // point from which the popup should open, relative to the iconAnchor
          });
			          var marketIcon = L.icon({
              iconUrl: 'market.png', // url that links to the icon image file
              iconSize:     [38, 38], // size of the icon image in pixels
              iconAnchor:   [19, 19], // the top left corner of the icon will be aligned so that this point is at the marker's geographical location
              popupAnchor:  [0, -10] // point from which the popup should open, relative to the iconAnchor
          });
		  			 var oipIcon = L.icon({
              iconUrl: 'oip.png', // url that links to the icon image file
              iconSize:     [38, 38], // size of the icon image in pixels
              iconAnchor:   [19, 19], // the top left corner of the icon will be aligned so that this point is at the marker's geographical location
              popupAnchor:  [0, -10] // point from which the popup should open, relative to the iconAnchor
          });

          var marker1 = L.marker([40.758896,-73.985130], {icon: timeIcon}).addTo(map);
         
		  var marker2 = L.marker([39.7641847,-86.1614069], {icon: oipIcon}).addTo(map);
		  var marker3 = L.marker([39.9659592,-83.0046041], {icon: marketIcon}).addTo(map);
		  
			
			
			marker1.bindPopup("TIMES SQUARE");
			marker2.bindPopup("Sheraton Indianapolis City Centre Hotel");
			marker3.bindPopup("North Market Downtown");
			var pic1 = '<img src="https://upload.wikimedia.org/wikipedia/commons/b/b8/US053_Times_Square_NY_1963.jpg" alt="TIMES" width="250">';
			var pic2 = '<img src="https://upload.wikimedia.org/wikipedia/commons/d/d2/Exterior_of_the_Birch_Bayh_Federal_Building_%26_U.S._Courthouse_-_May_2016_-_Artistmac.jpg" alt="Hotel" width="250">';
			var pic3 = '<img src="https://upload.wikimedia.org/wikipedia/commons/4/41/North_market_christmas.jpg" alt="Market" width="250">';

			marker1.bindPopup(pic1);
			marker2.bindPopup(pic2);
			marker3.bindPopup(pic3);
			var pic1 = '<img src="https://upload.wikimedia.org/wikipedia/commons/b/b8/US053_Times_Square_NY_1963.jpg" alt="TIMES" width="250">';
			var pic2 = '<img src="https://upload.wikimedia.org/wikipedia/commons/d/d2/Exterior_of_the_Birch_Bayh_Federal_Building_%26_U.S._Courthouse_-_May_2016_-_Artistmac.jpg" alt="Hotel" width="250">';
			var pic3 = '<img src="https://upload.wikimedia.org/wikipedia/commons/4/41/North_market_christmas.jpg" alt="Market" width="250">';
			marker1.bindPopup('TIMES SQUARE' + '<br>' + pic1);
			marker2.bindPopup('Sheraton Indianapolis City Centre Hotel' + '<br>' + pic2);
			marker3.bindPopup('North Market Downtown' + '<br>' + pic3);
			var pic1 = '<img src="https://upload.wikimedia.org/wikipedia/commons/b/b8/US053_Times_Square_NY_1963.jpg" alt="TIMES" width="250">';
			var pic2 = '<img src="https://upload.wikimedia.org/wikipedia/commons/d/d2/Exterior_of_the_Birch_Bayh_Federal_Building_%26_U.S._Courthouse_-_May_2016_-_Artistmac.jpg" alt="Hotel" width="250">';
			var pic3 = '<img src="https://upload.wikimedia.org/wikipedia/commons/4/41/North_market_christmas.jpg" alt="Market" width="250">';
			marker1.bindPopup('<p style="color:blue; font-weight:bold"> TIMES SQUARE </p>' + pic1);
			marker2.bindPopup('<p style="color:red; font-weight:bold"> Sheraton Indianapolis City Centre Hotel</p>' + pic2);
			marker3.bindPopup('<p style="color:green; font-weight:bold"> North Market Downtown</p>' + pic3);
			
			
			
        </script>
   </body>
</html>
