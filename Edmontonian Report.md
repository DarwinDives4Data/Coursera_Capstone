Edmontonian

### A. Introduction
The City of Edmonton is the capital of the Canadian province of Alberta and is home to about 1 million residents. Covering an area of approximately 767 square kilometres across 400 neighbourhoods, the population density is 1215 per square kilometre [1][2]. As a new resident of Edmonton, I choose to study Edmonton for this project.

The population density of Edmonton is one of the lowest of Canada's major cities. This seems to continue decreasing, where the city recently acquired 82.6 sq-km in low populace towns of Leduc County and the City of Beaumont in 2019 [1]. This low population density is a strong indicator of urban sprawl. This term is synonymous with many, many urban issues, such as increasing commuting time, increasing social isolation, decreasing farmland availability, increasing distance to access social venues, and an overall stress on sustainability. Not only does this put a large financial strain for the city, the costs will be shared with the residents in increasing property taxes, utility fees, road maintenance, infrastructure upgrades and social services. However, it is difficult to obtain the information to guide city planners, investors, and prospective residents towards a sustainable solution.
[1] Edmonton, Wikipedia https://en.wikipedia.org/wiki/Edmonton [2] City of Edmonton open datasets

### A2: The Problem
In consideration of these problems and to guide city planners and investors toward city densification, this project will use maps and charts to investigate the unique venue types and age groups clustered by neighbourhoods in Edmonton.

### A2: The Data
To process the data, IBM Watson Studio platform is used to express the Python language to process the data.
For data of the most common venues per neighbourhood, Foursquare API is used.
City of Edmonton neighbourhoods data: https://data.edmonton.ca/api/views/3b6m-fezs/rows.json?accessType=DOWNLOAD
City of Edmonton neighbourhoods age groups: https://data.edmonton.ca/api/views/a6zx-dzqn/rows.json?accessType=DOWNLOAD
Used for latitude/longitude of the centroid of neighbourhoods

## B: Methodology
For this project, Github was used to story the data related to this project. This includes the Jupyter Notebook (file type ipynb) and IBM Watson Studio. As this is a preliminary data analysis on Edmonton, the results are limited to venue exploration and clusters.

### B1: Data scraping
Data is found in tabular format through the City of Edmonton Website, with a JSON file.
This was used with the Python package pandas.

### B2: Assigning Geolocation Data
Latitude and longitude of each neighbourhood were collected from the City of Edmonton JSON files.
Foursquare API was used to identity the venues closest to each neighbourhood.
Mapping was used with Folium for visualization.

### B3: Examining the neighbourhoods
Using Foursquare API, using onehot encoding (1 for True, 0 for False) per venue, to find the probability of venue categories per neighbourhood. This mean will be used to rank the common venues in each neighbourhood. A dataframe with the 5 most common venues were made.

### B4: Neighbourhood Clustering
Using k-means clustering, the simulation found the value of K to be 2. Seems like

## Results and Discussion
As a preliminary analysis, there are just two clusters.
Cluster Label 1 containers 19 neighbourhoods having a high density of Fried Chicken, Filipino Restaurants, and Flower Shops.
Cluster Label 0 containers 381 neighbourhoods with a varied mixed of venues.

Further analysis shows that 6 of 19 in Cluster 1 had the following low density neighbourhoods (Hagmann Estate Industrial, Anthony Henday Big Lake, Anthony Henday South Blackburne, Place La Rue, Youngstown Industrial, and Southeast Industrial)

## Conclusion
This venue and distribution may be too small, and requires further analysis in exploring data relating to a multi-variable study such as urban sprawl. (It may be said that urban sprawl is...a "broad" topic.)
