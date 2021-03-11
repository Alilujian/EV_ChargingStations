# EV_ChargingStations
A Spatial Analysis of New York City Electric Vehicle Charging Stations

## Background
In 2018, there are 28% of the greenhouse gas produced by transportation. Within this sector, about 59% of the GHG is produced by light-duty vehicles (e.g., passenger cars) (EPA, 2020). Increasing the number of zero-emission electric vehicles in the city is a crucial element of New York City fighting climate change. The New York goal is to deploy 850,000 electric vehicles by the end of 2025 (Hundt & Schub, 2015). Achieve this goal will increase the number of electric vehicle (EV) charging stations since a better charging network can reduce range anxiety (Funke et al., 2019). Due to technological improvement, the expense of owning an electric vehicle has been drop. The most critical factor for the consumer to consider having an EV would be the convenience of charging their vehicles. According to the review by Hardman et al. (2018), about 50-80% of the charging events for EV occur at home. The second-largest proportion, about 25% of the charging event, occurs at work. Only about less than 10% of the charging events occur at public charging locations because they lack charging infrastructure.

## Objective
This paper will examine the location and spatial pattern of the current electric vehicle charging infrastructure in New York City. Also, determine the factors that influence consumers buying electric cars by doing a literature review. This paper aims to utilize GIS and spatial analysis tools to find out suitable places to build new electric vehicle charging infrastructure in the Bronx area. As a result, it creates a map showing all appropriate locations for building new charging stations in New York City.

## Method and Data
This study began by conducting a relevant literature review to determine consumer preferences for EV charging events. Understanding consumer preferences help determine suitable places for EV charging stations.\
A geographic information system (GIS) is a powerful tool to analyze spatial patterns and relationships. This paper will use GIS and related spatial analysis methods to create maps that show the suitable location for building a new EV charging station. When choosing a new location, factors that are considered are the land use conditions and proximity to the existing stations.\
The New York City (NYC, in short) refers to the five boroughs, which is The Bronx, Brooklyn, Manhattan, Queens, and Staten Island. This paper will examine the spatial pattern of charging stations in the whole NYC area and each borough. This will be done by applying Ripley’s K function and standard deviation ellipse to the point data set. Comparing the observed k value with the confidence envelope,  we can identify its spatial pattern. Generally, a spatial clustering pattern occurs because of the observed k value greater than the two confidence envelopes or vice versa. When observed k lie between the confidence envelops, it tells a random pattern.\
Information about the current EV charging infrastructure will be acquired from the New York Open Data website. Census, borough boundary, and other geography information of New York City can be accessed through the New York City data dropbox.\
XY table to point tools is used to load the EV charging station location table from a CSV file into a map. ‘Select by location’ tool allows us to exclude data point that is outside the study area. Dasymetric mapping helps us visualized the population density in each borough.\
Proximity analysis (Euclidean Distance) will allow us to see the distance between the current EV charging stations. The result of  Euclidean distance will then be reclassified into ten different classes. With the greater distance between stations, the assigned weight will be higher. Areal interpolation (weighted overlay) will allow us to overlay the land use raster with the Euclidean distance result. Only public accessible (or public owned) land (shown in the figure below) will be weighted in this paper.  Location with weighted overlay results greater than (or equal to) 7 will be considered suitable.

## Results
As a result of density analysis, from Figures 3 and 4, the population density is higher in the Manhattan and Bronx borough, and the total population is greater in the city center than in the rural area. Observation from the EV charging stations map (figure 5) suggests the EVC stations are clustered in the Manhattan area. By applying Ripley’s k function (figure 6), the results prove that the EVC stations are significantly clustering in a small distance in NYC, Manhattan, Brooklyn, and Queen. In the Bronx and Staten Island, the EVC stations are located more randomly (or disperse) than other boroughs.\
The Euclidean Distance map (figure 7) shows a higher value are located mostly at the edge of the borough boundary. Higher value, in this case, refers to a greater distance from an existing EV charging infrastructure. When overlay with land use raster layer, the potential location for a new EV charging station shows in the following map (figure 8, 9, 10, 11, 12). As a summarized result (table 1), Manhattan and Brooklyn area has the highest number of existing EV charging stations but the least area for building new stations. The Bronx and Staten Island have the lowest number of current charging infrastructure. Their suitable area adds up to 60% of the total potential area in NYC. On the other hand, Queen has a medium number of existing charging stations, but it still has enough space for building new infrastructure.

## Discussion
Public EV charging stations are public access and located on public land. In this paper, we only consider the publicly owned land to be a suitable location for building new charging stations. In our analysis, land classified as public facilities, vacant land, transportation, open space, and parking facilities will be considered publicly owned. When people charge their cars in the parking area, they tend to leave their cars in the parking. So that one charging station might require many charging infrastructure to fulfill the demand. Since the information about the existing number of electric vehicles in NYC is missing, it is hard for us to determine which area needs more infrastructure. Here we will assume the relationship between EV number and population is positive. This means a borough with a higher population will have a higher number of EVs. The results from our analysis state that the city center has a higher population than the rural area. Thus, the demand for new EV charging stations will be higher in the central part.\
Using 30 input features is an idea for doing Multi-Distance spatial cluster analysis (Ripley’s K function). The current EV stations in Staten Island and the Bronx area are less than 30. The cluster analysis for these two boroughs might not be as accurate as the other borough. Besides, only analyzing data points within our study area leads to the edge effect. For this reason, a result near the edge of a borough boundary might be least accurate.\
When using the weighted overlay, this paper only considers the land use condition and the proximity to existing EV charging stations. However, for real-world transportation planning, there might be more factors that need to be considered. The electric supply network might be a huge factor affecting the location of an EV charging infrastructure. The area with a high slope is hard for installing electric wiring so that it might not build charging infrastructure. Another critical factor is range anxiety. The consumer tends not to consider an electric vehicle if they cannot assure there are enough convenient charging stations (Henry et al., 2016). Moreover, more research is needed to find out the optimal distance between charging stations.

## Conclusion
Light-duty vehicles contribute about 50% of greenhouse gas emissions. To accelerate the transition to cleaner transportation mode in NYC requires a more extensive EV charging network. Current EV charging stations are located clustered around the Manhattan area in New York City. A total area of 8.8 square kilometers is suitable for building new EV charging stations in NYC. The space in Queen, Bronx, and Staten Island accounted for 90% of the total suitable area. New infrastructure can consider building in these boroughs.\
However, this result only considers a small part of the factors that influence location selection. The limitation mentioned above in the discussion will require a workable solution. Also, more consumer preference, policy legislation, and real-world implications will require further study in the future.





