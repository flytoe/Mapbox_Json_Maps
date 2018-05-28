Show route with Start, Stop-in-between and Stop in Audi Map Style


# 0. Google Directions API and GPSIES
You can use google maps directions to generate json
[https://developers.google.com/maps/documentation/directions/intro?hl=de#Waypoints][1]
Just convert this after you have entered your api key in [https://www.gpsies.com/convert.do][2] and download the ready route. Continue with step 5 … but if you want to get a more detailed route start with 1

# 1.Create location data and routes 
- Use [https://www.gpsies.com][3]
- Create map with “follow roads” and “car” checked
- Name track and download as .kml

# 2. Convert KML to GeoJson
- Use [https://mapbox.github.io/togeojson/][4] to convert

# 3. Check GeoJson
- Use [http://geojson.io/][5] to display data on a map and edit params to check if data is correct. Also Bboxes can set here.

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



[1]:	https://developers.google.com/maps/documentation/directions/intro?hl=de#Waypoints
[2]:	https://www.gpsies.com/convert.do
[3]:	https://www.gpsies.com/mapUser.do?username=flytoe "https://www.gpsies.com"
[4]:	https://mapbox.github.io/togeojson/
[5]:	http://geojson.io/#map=12/48.0353/16.6762 "http://geojson.io/"