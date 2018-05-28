Show route with Start, Stop-in-between and Stop in Audi Map Style

# 1.Create location data and routes 
- Use [https://www.gpsies.com](https://www.gpsies.com/mapUser.do?username=flytoe "https://www.gpsies.com")
- Create map with “follow roads” and “car” checked
- Name track and download as .kml

# 2. Convert KML to GeoJson
- Use [https://mapbox.github.io/togeojson/](https://mapbox.github.io/togeojson/) to convert

# 3. Check GeoJson
- Use [http://geojson.io/](http://geojson.io/#map=12/48.0353/16.6762 "http://geojson.io/") to display data on a map and edit params to check if data is correct

# 4. Save GeoJson and edit
remove gpsies header in Json and replace to the first coordinates.
	{
	    "type": "FeatureCollection",
	    "features": [
	        {
	            "type": "Feature",
	            "geometry": {
	                "type": "LineString",
	                "coordinates": [
						[	16.39808,
		                    48.20556,
		                    …

 Put this after the last number:

	                        48.20273,
	                        191
	                      ]
	                    ]
	                  }
	                }]
	              }

# 5. Add Routes to html file and updates params

# 6. Show routes by editing the variable “displayroute” to the desired route