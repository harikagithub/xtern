i have downloaded data using a data scrapping extension.

I tried downloading it through googleAPI but wasn't successful but still want to perform the analysis so dowladed it

now the data has 120 rows and 6 columns.i dropped the rows with null values because feedback cannot be imputed based on other factors and these were the results of my search "stores and places in indianapolis" in googlemaps.

presenting a one day plan from 9:00 A.M. to 9:00 P.M. must be time-effcient. so i choose to classify it based on two factors:
1.rating 
2.distance 

but for distance based classification we either need the distance or locate it on map and find it.
to locate it on map we need the location parameters such as latitude and longitude.

we can get the location parameters using geopy and geopandas

now lets plot our data on map using folium.
we plotted all our data points using folium.marker and can observe that there are few places far from the center of indianapolis. lets consider them as outliers because travelling to that particular point takes lot of time and there are very few places nearby so its not optimum to travel to those places.

lets start filtering data using rating. we will just go to the places with rating>4.4

it returned 69 stores with rating>=4.4

now lets mark them on map using folium. lets draw a circle within 3kms to make it more time-efficient and consider the remaining as outliers

and we now explore keeping the above factors in mind.
