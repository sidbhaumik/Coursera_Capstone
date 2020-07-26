## Indian Food Options in Major US Tourist Cities

### Introduction/Business Problem

Mr. Kumar from India has to attend a work conference in Boston, United States next month. Family vacation has been overdue for long so he decides on taking his wife and kids along with him. Along with Boston, he has picked Orlando, Florida as one of the destination to spend time with family.
His kids are crazy for Disney, so Orlando was an obvious choice. 
Now with the remaining time, he can only pick one tourist location out of 4 choices:
- Chicago 
- Miami
- New York
- Los Angeles

Kumar's wife is a big time foodie and specially obsessed with Indian foods. Since all 4 cities have their own set of attractions, So, she decides on picking the 3rd spot based on Indian restaurants.

The problem we aim to solve is to find the best U.S city out of 4 mentioned above for Indian restaurants and the best place out of the selected city to book a hotel.

### Data Section

I will use the FourSquare API through venues channel to collect data about locations of Indian Restaurants in 4 major U.S cities mentioned below: 
- Chicago,IL
- Miami, FL
- New York, NY
- Los Angeles,CA. 


### Methodology

My goal is to find the best city out of 4 given choices with the highest Indian restaurants density. For this, I have used the Four Square API through the venues channel. I used the near query to get venues in the cities. 
Also, I have used the CategoryID 4bf58dd8d48988d10f941735 to show only Indian restaurants. 

Foursquare limits us to maximum of 100 venues per query. I repeated this request for the 4 U.S cities and got their top 100 venues. I only saved the name and coordinate data from the result and plotted them on the map using Folium for visual inspection.

Next, to get an indicator of the density of Indian restaurants, I calculated a center coordinate of the venues to get the mean longitude and latitude values. Then I calculated the mean of the Euclidean distance from each venue to the mean coordinates. This was my indicator - mean distance to the mean coordinate.



### Results

From the initial visual inspection through the generated Maps, I see that they all have multiple Indian restaurants specially New York, Los Angeles & Chicago. Following are the pictures of the geoplot generated with folium:

### Chicago, IL

![Chicago%20geoplot1.png](attachment:Chicago%20geoplot1.png)

### Miami, FL

![Miami%20geoplot1.png](attachment:Miami%20geoplot1.png)

### New York, NY

![NewYork%20geoplot1.png](attachment:NewYork%20geoplot1.png)

### Los Angeles, CA

![LA%20geoplot1.png](attachment:LA%20geoplot1.png)

Initial inspection reveals New York, Chicago & Los Angeles are densely populated cities. But, to get more clarity I calculate the mean coordinate and the "Mean distance to Mean coordinate". The mean coordinate is displayed with a red circle and distances with dark green lines.

### Chicago, IL 
"Mean distance to Mean coordinate" :: 0.054875

![Chicago%20geoplot3.png](attachment:Chicago%20geoplot3.png)

### Miami, FL 
"Mean distance to Mean coordinate" :: 0.100926

![Miami%20geoplot3.png](attachment:Miami%20geoplot3.png)

### New York, NY 
"Mean distance to Mean coordinate" :: 0.025217

![NY%20geoplot3.png](attachment:NY%20geoplot3.png)

### Los Angeles, CA 
"Mean distance to Mean coordinate" :: 0.098707

![LA%20geoplot3.png](attachment:LA%20geoplot3.png)

#### Based on the "Mean distance to Mean coordinate" values, New York tops the chart followed by Chicago.

### Discussion

I observed the number of Indian Restaurants is highest in New York followed by Los Angeles. But, based on "Mean distance to Mean coordinate", Chicago ranks much higher than Los Angeles but still way behind New York.



### Conclusion

There is no doubt that New York is the clear winner here with so many Indian restaurants and so close to each other.

Also, it's highly recommended for our tourist to book a hotel close to the mean coordinate to have a delicious vacation. :)
