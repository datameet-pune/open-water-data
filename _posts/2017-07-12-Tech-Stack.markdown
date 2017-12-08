---
layout:     post
title:      Open Water Data Web Application
author:     Namita Bhatawdekar
<!-- tags: 		water data available -->
subtitle:  	The Tech Stack
category:  Tech
---
<!-- Start Writing Below in Markdown -->
The Open Water Data (OWD) web application aims to give researchers or anyone interested about water easy access to water data for their area of interest in India. 

# Design Criteria
While designing the web application, we have chosen to focus on a few key design criteria. These aren't meant to be a comprehensive list and some of these are guiding principles for features yet to be  implemented in the web app. 

### *Smooth Intuitive User Experience*
We are seeking to ensure a smooth user experience for anyone using the application even with internet bandwidth limitations. This criteria may in some cases affect the time-range of available data that can be viewed at one time or sometimes the spatial area of the visualization. Data caching may also be used to improve the rendering time for the data. 

### *In browser data analysis*
The app is also meant to provide the user a good range of geo-spatial functionality to interact and play around with the data in the browser itself, rather than offering just simple data visualizations with no possibility for deeper exploration.

### *Localized User Interface*
Another focus area was for the UI to be intuitive and accessible in local languages. For the data to find wider usage this would be absolutely essential.

### *Replicability*
Lastly and equally important was the modularity and replicability of the code to allow others interested to expand or spin off ideas built on this platform. This essentially required a web app that was built on open source libraries and code. 

### *How it works*
With these design criteria in mind we’ve put together the initial building blocks of the app.

![Description](http://datameet-pune.github.io/open-water-data/img/Water App Architecture Diagram.png)

The OWD application uses Google Earth Engine (GEE) at its core to store and process raw earth observation satellite data producing water datasets as per user requests for their area of interest. Since the core product is Google's it also fit best to use other Google infrastructure such as Google Maps and Google App Engine.

The [OWD web application code](https://github.com/datameet-pune/open-water-data-app) is hosted on Google App Engine and it includes the Earth Engine Python library. The OWD app can hence make Earth Engine requests from App Engine using a [service account](https://developers.google.com/earth-engine/service_account) which allows the user of the app to view data in their browser without requiring a login. 

OWD also uses the Google Maps API to render these Earth Engine visualizations which are rendered as Google Map overlays. Google maps also provides customization features such as localization to view the map in different languages and search to find locations of interest.



# The App Engine Server Framework

### Webapp2
The application server is built along the same lines as Google Earth Engine 
pplications using [webapp2](https://webapp2.readthedocs.io/en/latest/#), a Python web framework for Google App Engine. This is primarily due to its ready compatibility with Google App Engine and the availability of Google Earth Engine’s [demo applications](https://github.com/google/earthengine-api/tree/master/demos). The framework is supported by Google though they do not directly maintain it. Most of the documentation in App Engine refers to webapp2 for examples. The app server uses the Earth Engine Python library and the service account specified in config.py. The Python API in the server.py file does most of the communication with Earth Engine. 
The [OWD web application code](https://github.com/datameet-pune/open-water-data-app) is also being hosted on Github both for version control and to keep with the open source principle of this platform


### Jinja2
When a user loads the application in their browser, the Main Handler in server.py serves index.html with the [Jinja2](http://jinja.pocoo.org/) templating engine. On selecting a dataset layer, a request is sent to the server to fetch corresponding data from Earth Engine using the Python API. The map information is then returned to the client script to render an Earth Engine map as a Google Map overlay.

# The Client Framework
While the Earth Engine overlay information is received from the server, the client still talks directly to Earth Engine to load map tiles. Client is built using the React-Redux framework.

### React-Redux
The front-end components are built using [React](https://reactjs.org/). Between React.js and Angular.js, Angular is a full framework whereas React is a small view library and provides more flexibility that satisfies the  features needed in our web application. React framework is specifically about fast view rendering. If a page has many dynamic components the DOM has to be frequently updated and these frequent updates can slow down rendering. React allows re-rendering of only the changed DOM elements hence proving to be much faster. Our application is not back-end heavy hence React (front end only) seemed like a great choice to build and maintain the application. Since React is only the front-end View layer, we use [Redux](https://redux.js.org/) to maintain the application state and perform any AJAX calls. 

In addition, we also use [NPM](https://www.npmjs.com/) and [Webpack](https://webpack.github.io/) to build the client-side application.

### NPM
NPM is a node package manager that helps in installing and maintaining node package versions.

### Webpack
Webpack is a module bundler. It processes the application and includes all the modules needed by our application. These modules are packaged as a single bundle.js file that is loaded in the browser.

## Code

Inline `code`.

{% highlight python %}
import numpy as np
def hello_world():
    print('Hello World!'')
{% endhighlight %}


