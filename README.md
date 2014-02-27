# Table of contents
* [Overview](!overview)
* [CartoDB](!introduction-to-cartodb)
* [PostGIS](!postgis)

# Overview

This workshop is first and foremost and introduction to PostGIS and the power of geospatial processing with open source tools. To get you there quickly, we are using the CartoDB platform. CartoDB is an open source tool that uses PostGIS to create dynamic interactive maps. CartoDB runs directly in the browser, allowing us to avoid having to install PostGIS during this introduction workshop.

##### Who

* [Michael Keller](https://twitter.com/mhkeller)
* [Andrew Hill](https://twitter.com/andrewxhill)

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


### Using the dashboard

The CartoDB dashboard is broken down into a few different interfaces. 

##### The table manager

This is the first page you see when you load your account. It is where you will drag new files for upload or create new blank tables. You can see and delete existing datasets here.

##### The table view

When you load a new dataset or load an old one, you'll be brought to the table view. The table view lets you look at the ```columns``` and ```rows``` of your data. You can edit individual values. You can change column names and types. You can filter your data and query it using ```SQL```.

##### Map view

From any table, you can click ```Map``` to see the map of the data. As long as your data contained some geospatial information, it should appear on the map. From here, you can style and edit your geospatial data. It is a good place for prototyping published visualizations.

##### Visualization

Whenever you want to publish a map or combine multiple map layers into a single map to be published, you'll create what is called a ```Visualization```. Visualizations live above maps and tables. They are linked directly to the data in your tables, but you can change the styles and filters of a visualization as much as you like. Visualizations do not take up more space on your account. So from one dataset, you can publish many visualizations.

##### Visualization manager

Just like your table manager, there is a page for you to see all your visualizations. You can also delete visualizations. Deleting a visualization will not remove the underlying table or map. 

### Importing data

Importing data into CartoDB is easy! All you need is a file in a supported format (CSV, KML, GeoJSON, and Shapefile are all good ones) either online or on your desktop. You can drag local files right to your browser to import. Remote files you can import by pasting the URL into the import field.

#### Datasets

| File          | Dataset name     | Geom type |
| ------------- |:----------------:|:---------:|
| [counties_ne.zip](http://csvsoundsystem.github.io/nicar-cartodb-postgis/data/counties_ne.zip) | Nebraska Counties   | polygons |
| [postoffices_ne.zip](http://csvsoundsystem.github.io/nicar-cartodb-postgis/data/postoffices_ne.zip) | US Post Offices | points |

##### Four ways to get data into CartoDB

1. Drag and drop a file or a ZIP to you dashboard
2. Import from a URL
3. Add new data to a row in your tables or by drawing on the map
4. Use authenticated [SQL API](http://developers.cartodb.com/documentation/sql-api.html) calls to write data

![import](http://csvsoundsystem.github.io/nicar-cartodb-postgis/assets/gifs/import.gif)

#### First data import

Let's start by importing the dataset of Nebraska Counties.

1. Right click the [counties_ne.zip link](http://csvsoundsystem.github.io/nicar-cartodb-postgis/data/counties_ne.zip), copy URL to clipboard
2. Go to your CartoDB dasboard in the table manager
3. Click ```New table```
4. Paste the data URL into the form field
5. Click ```Create table```

## Creating maps

### Basic map styling

##### Choropleths, Category maps, Bubble maps

![styling](http://csvsoundsystem.github.io/nicar-cartodb-postgis/assets/gifs/styling.gif)

There are many styles possible in CartoDB. The tool includes a simple style wizard for you to apply and customize just some of these. When you grow out of the wizard, you'll want to dig into the CSS editor to really customize your maps.

##### Infowindows and legends

You can add infowindows and legends to any maps you create. There are some nice simple tools for you to create and customize. As you learn more though, you can also take advantage of full HTML templating to make them look and behave exactly as you want.

![infowindows and legends](http://csvsoundsystem.github.io/nicar-cartodb-postgis/assets/gifs/legends.gif)

### Visualizations

Let's start by importing the second dataset of Nebraska Post Offices. Go back to your table manager, then

1. Right click the [postoffices_ne.zip link](http://csvsoundsystem.github.io/nicar-cartodb-postgis/data/postoffices_ne.zip), copy URL to clipboard
2. Go to your CartoDB dasboard in the table manager
3. Click ```New table```
4. Paste the data URL into the form field
5. Click ```Create table```

Now that we have our Post Office dataset, let's create a visualization. You do this by clicking the ```VISUALIZE``` button in the upper right. Next, give your visualization a name. This will take you to a new visualization where you can publish you can finalize design, add new layers, or publish your map.

### Combine layers

Visualizations allow you to mix multiple datasets into a layered map. You can add a new layer by clicking the plus sign directly above the right-hand menu.

![infowindows and legends](http://csvsoundsystem.github.io/nicar-cartodb-postgis/assets/gifs/layers.gif)

You can reorder the layers on the map by dragging layers up through the stack. Each layer can be styled and edited independantly. You can also add interactivity and legends for the layers. 

### Publish maps

Right away you can get a public link for your visualization. Where the button ```VISUALIZE``` used to be, it should new say ```PUBLISH```. From there you can get the menu for publishing maps.

![infowindows and legends](http://csvsoundsystem.github.io/nicar-cartodb-postgis/assets/gifs/visualize.gif)

##### Links, embeds, CartoDB.js

Publishing maps can be as simple as getting the sharable URL. The interface also gives you an ```embed``` option for adding maps to your blog or website. It also has an ```API``` option, for using your visualization with our [CartoDB.js](http://developers.cartodb.com/documentation/cartodb-js.html) library. CartoDB.js will allow you to integrate highly customized maps directly into your website. For now, sharable URLs and map embeds should get you pretty far.

# PostGIS

PostGIS is an extension for the open-source database PostgreSQL. It's a "spatially-aware" database. For example, let's say you have a spreadsheet with a latitude and a longitude column. To a normal database, those are just numbers. To PostGIS, it knows they are geography, which lets you do things like find all points within a certain radius of a given point, or calculate the distance from these points to other things.

## Installation

Follow [these guidelines](https://github.com/csvsoundsystem/nicar-cartodb-postgis/blob/gh-pages/SETUP.md#installing-postgis-locally) on how to set up PostgreSQL and PostGIS on your own machine.

## Operators


* `AND`
* `OR`
* `>`
* `<`
* `=`
* `IS NULL` e.g. `SELECT * FROM tbl WHERE year IS NULL`
* `IS NOT NULL` e.g. `SELECT * FROM tbl WHERE year IS NOT NULL`

### Special Operators

Indexed nearest neigbhor search. We'll get to this below.

* `<->`
* `<=>`

### Filtering, ordering, limiting

Let's start working with historic Post Offices in Nebraska: `postoffices_ne`.

Click on the `SQL` tab we can start doing some basic querying.

##### Filtering: `WHERE`

SQL can filter using the `WHERE` command.

````
SELECT * FROM postoffices WHERE year < 1900

SELECT * FROM postoffices WHERE year > 1900 AND year < 1920 AND daily_customers > 100

SELECT * FROM postoffices WHERE year > 1900 OR daily_customers < 100

SELECT * FROM postoffices WHERE (year > 1900 AND year < 1920) OR daily_customers > 100
````

##### Ordering: `ORDER BY`

Order by year made

````
SELECT * FROM postoffices_ne ORDER BY year

SELECT * FROM postoffices_ne ORDER BY year DESC
````

You can also set `ASC` for ascending, which is the default.

##### Limiting: `LIMIT`

Instead of showing every row, you can limit your query. This can be useful to make your queries faster or decrease the files size of your data export.

Grab the first five

````
SELECT * FROM postoffices_ne LIMIT 5
````

This data isn't in any order though, so that query isn't very helpful. This will grab the five oldest.

````
SELECT * FROM postoffices_ne ORDER BY year LIMIT 5
````

### Selecting, counting

##### Selecting

We've been doing `SELECT` statements to create a view on our database. You might have noticed the `*`, which means "Get all columns". You can also only retrieve specific columns by name.

````
SELECT name, year, daily_customers FROM postoffice_ne LIMIT 10
````

Because this is a spatially-aware database, we also have a column that holds our lat/lng. PostGIS usually refers to this column as `geom` or `the_geom` in CartoDB.

````
SELECT name, year, daily_customers, the_geom FROM postoffice_ne LIMIT 10
````

##### Counting

Let's say you want to know some aggregate information, like how many rows you have

````
SELECT count(*) FROM postoffice_ne

SELECT count(*) FROM postoffice_ne WHERE year > 1950
````

### Spatial joining with `ST_Intersects()`

Before, we joined two dataset based on a shared name. We had census tract shapes and a spreadsheet of census tract populations and we joined them on the census tract id.

But data doesn't come preaggregated like this. What if we want to make a choropleth from point data.

Let's make a make of Post Office density by county in Nebraska.

Open up `counties_ne` and run this query and let's add a column, call it, `postoffices` and set its type to `number`.

Run this query

````
UPDATE counties_ne SET postoffices = (
  SELECT count(*) 
  FROM postoffices_ne 
  WHERE 
  ST_Intersects(
    postoffices_ne.the_geom, 
    counties_ne.the_geom 
  )
)
````

More generically:

````
UPDATE name_of_polygon_table SET new_column_name = (
  SELECT count(*) 
  FROM name_of_point_table 
  WHERE 
  ST_Intersects(
    name_of_point_table.the_geom, 
    name_of_polygon_table.the_geom 
  )
)
````

Note: If you aren't using CartoDB, replace `the_geom` with `geom`.


### Mapping distance with `ST_Distance()` and `ORDER BY <->`

PostGIS is also really powerful for measuring distance, which can be a great story topic. Cezary Podkul did a great story a couple of years ago looking at Post Offices that were closing that were also far away from broadband access.

We can do this same calculation right here. We'll measure the distance from each Post Office to the nearest area that has broadband.

You can take a look at `broadband_ne`, which shows areas of Nebraska that have broadband access. We're actually going to be doing the measurement in `postoffices_ne` since that's the data we'll be modifying.

Create a new column in `postoffices_ne` called `dist` and set its type to `number`.

````
UPDATE postoffices_ne SET dist = (
  SELECT ST_Distance(
            postoffices_ne.the_geom, 
            broadband_ne.the_geom
          )
          FROM broadband_ne 
          ORDER BY postoffices_ne.the_geom <-> broadband_ne.the_geom 
          LIMIT 1
)
````

Or more generically:

````
UPDATE name_of_point_table SET new_column_name = (
  SELECT ST_Distance(
            name_of_point_table.the_geom, 
            name_of_polygon_table.the_geom
          )
          FROM broadband_ne 
          ORDER BY name_of_point_table.the_geom <-> name_of_polygon_table.the_geom 
          LIMIT 1
)
````
Note: If you aren't using CartoDB, replace `the_geom` with `geom`.


### Other fun functions

* [ST_MakeLine()](http://postgis.refractions.net/docs/ST_MakeLine.html)
* [ST_Distance()](http://postgis.refractions.net/docs/ST_MakeLine.html)
* [ST_MakeValid()](http://postgis.refractions.net/docs/ST_MakeValid.html)
* [ST_DWithin()](http://postgis.refractions.net/docs/ST_DWithin.html)
* [ST_Buffer()](http://postgis.refractions.net/docs/ST_Buffer.html)
* [ST_Intersection()](http://postgis.refractions.net/docs/ST_Intersection.html) - Similar to Clip in ArcMap: "Returns a geometry that represents the shared portion of geomA and geomB."

### Links, resources

* [PostGIS Documentation](http://postgis.net/docs/manual-dev/reference.html) - Read through the functions to see what it's capable of.

* [PostGIS Homepage](http://postgis.net/)

* [PostPostGIS](http://twitter.com/PostPostGIS) - A Twitter account that discusses geospatial analysis and critical theory.
