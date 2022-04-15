# Toronto Snow Plows 2022: Understanding Demand, Performance, Utilization and Public Sentiment

In January 2022, Toronto had one of the most severe snow-storm events from the 16-17th. There was +45 cm of snow, making this storm fall into the top 10 most severe snow events for the City. The City was not prepared for this event, and in addition to overspending on their operations also received much negative publicity from the media.

In this project, data was collected from the [City's PlowTO Map](https://www.toronto.ca/services-payments/streets-parking-transportation/road-maintenance/winter-maintenance/plowto/), an interactive map which has point-in-time data. This allowed us to have historical data on snow storm events in the month of February which  was collected, analyzed and combined with several data sources, to deliver an exploratory data analysis of this data answering questions in four main dimensions: performance, utilization, demographic trends and public perception.

**Overview of Files**
1. ```REST Server Downloader.ipynb```: Downloads from PlowTO Map REST Server and saves to JSON
2. ```Plow Data Pipeline.ipynb```: Parses PlowTO JSON files to shapefile and creates plots of plow utility
3. ```Weather Data Pipeline.ipnyb```: Parses Environment Canada data CSV files.
4. ```Plow TO Street```: Parses PlowTO JSON street files and saves GeoDataFrame.
5. ```Plow TO Street Map```: Reads GeoDataFrame and generates choropleth map, districts plowing graph and road type plowing graph.
6. ```Twitter Data Pipeline.ipnyb```: Connect to Twitter to Search Full Archive and Search User Timeline API endpoints and save into a Pandas dataframe. Performs Sentiment analysis.
7. ```Twitter Sentiment and Weather Data.ipynb```: Merges Twitter sentiment and weather information, generates visualizations per storm event.


**Overview of Data**:
* ```Snow Plow Data Sample``` - Feb 17th 8 PM - Feb 18th at 1 AM 
* ```src``` folder: then have all our data folders (Plow TO, weather, shapefiles, twitter, demographics) there 
* ```img``` folder: contain flow chart images for main project components
* ```Presentation-Snow Plow TO.pdf```: presentation showing the complete exploratory data analyses process

**Links to Medium Articles:**
* How to Download from an ArcGIS REST Server using Python - https://medium.com/@thomas.deboer/how-to-download-from-an-arcgis-rest-server-using-python-df900db3e364
* Choropleth maps with time sliders using Plotly - https://medium.com/@lucas_bromerchenkel/choropleth-maps-with-time-sliders-using-plotly-df6e19e5f90c
* Absolute Beginners Guide to Tweepy and the Twitter APIs - https://medium.com/@katia.ossetchkina57/absolute-beginners-guide-tweepy-and-the-twitter-apis-6070995efc63


**Workflow for Street Line Data:** 

![Workflow Street Line Data](/img/street_plow_pipeline.png)

**Workflow for Plow Point Data:**

![Workflow Plow Point Data](/img/point_plow_pipeline.png)

**Workflow for Twitter API Data:** 

![alt text for screen readers](/img/twitter_processing_pipeline.png "Text to show on mouseover")

