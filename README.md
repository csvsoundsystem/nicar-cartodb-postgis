# Table of contents
* [Overview](!overview)
* [CartoDB](!introduction-to-cartodb)
* [PostGIS](!postgis)

# Overview

This workshop is first and foremost and introduction to PostGIS and the power of geospatial processing with open source tools. To get you there quickly, we are using the CartoDB platform. CartoDB is an open source tool that uses PostGIS to create dynamic interactive maps. CartoDB runs directly in the browser, allowing us to avoid having to install PostGIS during this introduction workshop.

##### Us?

[Michael Keller](https://twitter.com/mhkeller)
[Andrew Hill](https://twitter.com/andrewxhill)

### Bonus

By the end of this workshop you will also have created a map with both Leaflet and Google Maps, you will have created infowindows and legends on an interactive map, and you will have created maps that you can embed and share on your websites or twitter.

# Introduction to CartoDB

[CartoDB](http://cartodb.com) is an open source tool hosted as an online service. Anyone can create a free account and for those more adventurous, the source is available on [GitHub](http://github.com/CartoDB/CartoDB).

![cartodb_intro](http://csvsoundsystem.github.io/nicar-cartodb-postgis/assets/gifs/cartodb_intro.gif)

#### Tutorials

You can find a long list of tutorials, both written and video, on [the CartoDB website](http://developers.cartodb.com/tutorials.html)

#### Documentation

As you learn more about CartoDB, start digging into the [online documentation](http://developers.cartodb.com/documentation/apis-overview.html)

CartoDB allows you to make more than just maps, it can help you build entire geospatial applications. There is an easy to use [Javascript library](http://developers.cartodb.com/documentation/cartodb-js.html) that you can use to integrate maps, geospatial data, and SQL queries into your website. 

#### Support

As you start expirementing more you'll want to know about the [GIS StackExchange](http://gis.stackexchange.com/questions/tagged/cartodb). If you tag questions with ```cartodb```, ```postgis``` or both you will get great help from the community. Just remember to keep question titles short and descriptive. Same goes for the question content, keep it short and to the point. Include links to code (preferably code that wont disappear in the future) or include portions of relevant code for potential helpers to better understand your problem.

### Importing data

#### Datasets

### Using the dashboard

## Creating maps

### Basic map styling

### Visualizing two datasets

### Name joins

... for census tracts, the column to join on is `nyc_tract_populations` in `nyc_tract_populations` and `ct2010` in `nyc_tracts2010`

## Publish maps

### Infowindows

### Legends

### Links, embeds, CartoDB.js

# PostGIS

## Installation

Follow [these guidelines](https://github.com/csvsoundsystem/nicar-cartodb-postgis/blob/gh-pages/SETUP.md#installing-postgis-locally) on how to set up PostgreSQL and PostGIS on your own machine.

### Filtering, ordering, limiting

### Selecting, counting, summing

### Spatial joining

### Mapping distance

... distance to nearest X, find me all within range of X

### Making lines from points

### Links, resources
