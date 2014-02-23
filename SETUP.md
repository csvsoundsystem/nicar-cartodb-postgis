TODO

[] Setup instructions for CartoDB

# Installing PostGIS locally

PostGIS is an extension on top the open-source database PostgreSQL.

[PostGIS.net/install](http://postgis.net/install/) has some good (and more detailed for other systems) instructions on how to get started. Generally, there are at least three ways to install PostgreSQL on Mac OS X. 

* Through Homebrew `brew install postgresql`
* Through the [Postgres app](http://postgresapp.com/)
* Through the [KyngChaos installers](http://www.kyngchaos.com/software/postgres)

It's a good idea to only use one of these methods, since mixing and matching can cause problems. Also, keep in mind that your PostgreSQL client can be a different version from your PostgreSQL server, which can cause problems if you're trying to use new features that aren't supported in older versions.

Once you have PostgreSQL installed, you access it by running `psql` in your terminal. You sometimes need to manually activate the PostGIS extension. PostGIS.net has some good instructions for how to do this for PostGIS (just one line) as well as for other handy spatial extensions:

````
-- Enable PostGIS (includes raster)
CREATE EXTENSION postgis;

-- Enable Topology
CREATE EXTENSION postgis_topology;

-- fuzzy matching needed for Tiger
CREATE EXTENSION fuzzystrmatch;

-- Enable US Tiger Geocoder
CREATE EXTENSION postgis_tiger_geocoder;
````
