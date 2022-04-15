# Toronto Snow Plows 2022: Understanding Demand, Performance, Utilization and Public Sentiment

Overview of Files

1. ```REST Server Downloader.ipynb```: Downloads from PlowTO Map REST Server and saves to JSON
2. ```Plow Data Pipeline.ipynb```: Parses PlowTO JSON files to shapefile and creates plots of plow utility
3. ```Weather Data Pipeline.ipnyb```: Parses Environment Canada data CSV files.
4. ```Plow TO Streets...```
5. ```Plow TO Street Map ...```
6. ```Twitter Data Pipeline.ipnyb```: Connect to Twitter to Search Full Archive and Search User Timeline API endpoints and save into a Pandas dataframe. Performs Sentiment analysis.
7. ```Twitter Sentiment and Weather Data.ipynb```: Merges Twitter sentiment and weather information, generates visualizations per storm event.



**Overview of Data**:

```Snow Plow Data`` - Feb 17th 8 PM - Feb 18th at 1 AM 

```src``` folder: then have all our data folders (Plow TO, weather, shapefiles, twitter, demographics) there 
```ima``` folder: contain flow chart images for main project components
```Presentation-Snow Plow TO.pptx```: presentation showing the exploratory data analyses process

Links to Medium Articles:
Choropleth maps with time sliders using Plotly - https://medium.com/@lucas_bromerchenkel/choropleth-maps-with-time-sliders-using-plotly-df6e19e5f90c
Getting Stated with Twitter API - 
____________________________________________________________________________________________________________________________________________________

    Street Data
For running the notebooks analyzing the street data:
First, you'll need to download the centreline dataset from Toronto's Open Data Portal. We couldn't fit it on github due to size constraints.
Download the GeoJSON, WGS84 projection from https://open.toronto.ca/dataset/toronto-centreline-tcl/
Place the file inside 'src/length_of_streets/'

To begin, run the notebook 'Street Data Parsing.ipynb'. It will iterate through the available snow plow data and create the necessary folders for the next step.
Next, run the notebook 'Street Data Map Pipeline.ipynb'. It will iterate over the available folder in the 'src' folder, and create an animated choropleth map, and two visualizations using seaborn. It might take a few minutes of run time.
Right now, there are only 3 timestamps since each raw timestamp takes up a lot of space. If you'd like to implement a similar project, check out the Medium articles linked at the top of this file and find out how to collect more timestamp data.

Workflow for Street Line Data: 
![Workflow Street Line Data](/img/Street Plow Pipeline.png)

Workflow for Plow Point Data: 
![Workflow Plow Point Data](/img/Point Plow Pipeline.png)

Workflow for Twitter API Data: 
![Workflow Twitter API Data](/img/Twitter Processing Pipeline.png)
