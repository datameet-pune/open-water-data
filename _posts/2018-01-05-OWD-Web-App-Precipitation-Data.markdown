---
layout:     post
title:      The Open Water Data Web App
author:     Namita Bhatawdekar
tags: 		Data App Precipitation
subtitle:  	Precipitation Data
category:  App
---
<!-- Start Writing Below in Markdown -->

The OWD web app is an initial proof of concept which takes this remote sensing based precipitation data and makes it available in an easy to use web interface for the user’s area and time period of interest. This represents a step forward in improving access by removing technical barriers to obtain precipitation data and also allowing data downloads rather than simply web visualization. 

Table of Contents
===================
  * [The Dataset](##The-Dataset)
    * [Specifications](###Specifications)
  * [Use Cases](##Use-Cases)
  * [Using the Web App](##Using-the-Web-App)
  * [Future Plans](##Future-Plans)
    * [Short term goals](###Short-term-goals)
    * [Long term goals](###Long-term-goals)
  
## The Dataset
The Open Water Data (OWD) Web App provides a web interface to view and download rainfall data for different watersheds for a selected time period of interest. The dataset from which rainfall data is derived is the CHIRPS dataset (Climate Hazards Group InfraRed Precipitation with Station data - version 2.0 final) which is a quasi global dataset of high resolution daily rainfall. 
This dataset is updated monthly based on an [algorithm](http://dx.doi.org/10.3133/ds832) published in 2014 by researchers at the United States Geological Survey (USGS) and the Climate Hazards Group (CHG) - University of California, Santa Barbara. The dataset makes use of a range of different satellite datasets for precipitation and in situ data from monitoring stations to arrive at a much more accurate estimate of daily rainfall.

The dataset is available under the public domain, allowing for its use and distribution even for commercial purposes for free and without permission. To cite this dataset it is recommended to use the following
Funk, C.C., Peterson, P.J., Landsfeld, M.F., Pedreros, D.H., Verdin, J.P., Rowland, J.D., Romero, B.E., Husak, G.J., Michaelsen, J.C., and Verdin, A.P., 2014, A quasi-global precipitation time series for drought monitoring: U.S. Geological Survey Data Series 832, 4 p., http://dx.doi.org/10.3133/ds832

### Specifications
**Link**: https://code.earthengine.google.com/dataset/UCSB-CHG/CHIRPS/DAILY<br>
**Time period**: January 1st, 1981 to December 1st, 2017.<br>
**Span**: Quasi-global (50 deg N to 50 deg S)<br>
**Format**: Gridded rainfall data<br>
**Spatial resolution**: 0.05 deg gridded data (i.e. approximately 5 km resolution)<br>
**Temporal resolution**: Daily<br>

## Use Cases
CHIRPS v2.0 can be used for local watershed level water resource planning by allowing users to create historical trend series for daily rainfall for upto 37 years. Data since 2000 for India is likely to be of higher accuracy since the [number of ground stations](ftp://ftp.chg.ucsb.edu/pub/org/chg/products/CHIRPS-2.0/diagnostics/stations-perMonth-byCountry/pngs/India.072.station.count.CHIRPS-v2.0.png) in the country incorporated into the CHIRPS dataset increased to more than 100. Besides this, since 1999 we have had dedicated satellite rainfall monitoring missions globally which have improved the accuracy of estimations. 

## Using the Web App
The OWD app can be accessed at: https://water-data-web-app.appspot.com/<br>
By default, data is fetched for the last 7 days for the whole of India.

|   |
|:---|
|**App Interface**: The app interface will appear as below|
|![app-interface](https://datameet-pune.github.io/open-water-data/img/app-interface.png)|
|**Select Dataset**: To view a dataset, toggle the dataset layer in the left sidebar. You will see a loading spinner while the data is being fetched|
|![select-dataset](https://datameet-pune.github.io/open-water-data/img/select-dataset.png)|
|**Tile Loading**: When the rainfall data has been fetched, the map tiles will start loading on the base map and you will be able to see the tile loading progress in the sidebar next to the selected dataset|
|![tiles-loading](https://datameet-pune.github.io/open-water-data/img/tiles-loading.png)|
|**Precipitation Layer Loaded**: When the all the tiles have finished loading, you will be able to see the selected dataset on the map. A legend on the right displays the map colors and corresponding dataset values|
|![precipitation-loaded](https://datameet-pune.github.io/open-water-data/img/precipitation-loaded.png)|
|**Date Selection**: You can further filter the dataset for a time period of your interest. To filter by a time period, select a Start date and End date from the side bar. Requests for a time range of more than 1 month generally takes time to load|
|![date-selection](https://datameet-pune.github.io/open-water-data/img/date-selection.png)|
|**Watershed Selection**: You can also filter the dataset for a watershed of your interest. This will fetch data for the selected watershed for the selected time period.To select a watershed, click on any of the displayed watersheds on the map|
|![watershed-selection](https://datameet-pune.github.io/open-water-data/img/watershed-selection.png)|
|**To Download**: You can download the your filtered dataset in a spreadsheet format (csv) using the Download button displayed next to the dataset toggle|
|![to-download](https://datameet-pune.github.io/open-water-data/img/download-highlight.png)|
|**Export in Progress**: You will be able to see a “Export in progress..” message displayed on top of the screen while your csv file is being prepared|
|![export-in-progress](https://datameet-pune.github.io/open-water-data/img/export-in-progress.png)|
|**Download Successful**: When your csv file is ready for download, you will get a message “Exported successfully” on top of the screen with your download link. Click on this link to download the csv file to your computer|
|![download-successful](https://datameet-pune.github.io/open-water-data/img/download-successful.png)|

## Future Plans
We wish to first prioritize building a community of users around this data. Primarily researchers, but also people within institutions that plan local management of water resources. This is mainly because datasets such as this would be new and unfamiliar to a larger audience, hence demonstrating a few use cases and comparisons with existing data available at the grassroots and government precipitation data would be vital.
Once this community of users i.e. a ‘working group or network on water data’ is established it can focus of improving the usability of the platform, adding features and datasets and making the data more usable at the grassroots level, for example by developing mobile apps, localization of the dataset etc.

### Short term goals
* Building user community
* __Upload feature__: to allow users to compare their own precipitation data with data available through the web app
* __Charts__: to visualize precipitation data time series in the browser
* __Improved watershed map of India__: The watershed map used currently in the app has no recognised source and is meant to be a placeholder till we have a better watershed map, i.e. a digitized version of CWC’s Watershed Atlas of India.

### Long term goals
In the long term we also seek to provide other datasets vital to water resource management planning at local levels. Stay tuned for updates.

Feel free to send us your feedback at pune@datameet.org
We also welcome collaborations from researchers in water resources, grassroots level implementing organisations, web developers, GIS/RS professionals etc.






