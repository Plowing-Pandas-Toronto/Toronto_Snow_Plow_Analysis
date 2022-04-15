# Toronto Snow Plow

Overview of Files
1 - QGis ...
2 - 
3- 
4 - Twitter
5- 



Organization:

Data Sources Folder

Overview of Data:

Snow Plow Data - Feb 17th 8 PM - Feb 18th at 1 AM 

src folder: then have all our data folders (Plow TO, weather, shapefiles, twitter, demographics) there 
images folder: have our flow charts there

PowerPoint online (main)

Readme structuring

Links to Medium Articles:
Choropleth maps with time sliders using Plotly - https://medium.com/@lucas_bromerchenkel/choropleth-maps-with-time-sliders-using-plotly-df6e19e5f90c

For running the notebooks analyzing the street data:
First, you'll need to download the centreline dataset from Toronto's Open Data Portal. We couldn't fit it on github due to size constraints.
Download the GeoJSON, WGS84 projection from https://open.toronto.ca/dataset/toronto-centreline-tcl/
Place the file inside 'src/length_of_streets/'

To begin, run the notebook 'street_data_parsing.ipynb'. It will iterate through the available snow plow data and create the necessary folders for the next step.
Next, run the notebook 'street_data_map_pipeline.ipynb'. It will iterate over the available folder in the 'src' folder, and create an animated choropleth map, and two visualizations using seaborn. It might take a few minutes of run time.
Right now, there are only 3 timestamps since each raw timestamp takes up a lot of space. If you'd like to implement a similar project, check out the Medium articles linked at the top of this file and find out how to collect more timestamp data.

