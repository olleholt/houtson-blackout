# houtson-blackout
for eds223 final proj

## Problem Statement

What impact did the Texas power outage have on different socioeconomic communities?

## Goals

"In February 2021, the state of Texas suffered a major power crisis, which came about as a result of three severe winter storms sweeping across the United States on February 10--11, 13--17, and 15--20."

Tasks for this analysis

-   estimating the number of homes in Houston that lost power as a result of the first two storms

-   investigating if socioeconomic factors are predictors of communities recovery from a power outage

**Highlights of Analysis:**

-   loading vector/raster data

-   simple raster operations

-   simple vector operations

-   spatial joins

### Data

**Night lights data**

Spatial data is remotely-sensed night lights data, acquired from the Visible Infrared Imaging Radiometer Suite (VIIRS) onboard the Suomi satellite. Specifically, VNP46A1 to detect differences in night lights before and after the storm to identify areas that lost electric power.

**Roads**

To minimize falsely identifying areas with reduced traffic as areas without power, areas near highways will be ignored. Geofabrik's download sites will be used to retrieve a shapefile of all highways in Texas and prepared a Geopackage (.gpkg file) containing just the subset of roads that intersect the Houston metropolitan area. 

**Houses**

We can also obtain building data from OpenStreetMap from Geofabrick and prepared a GeoPackage containing only houses in the Houston metropolitan area.

**Socioeconomic**

We cannot readily get socioeconomic information for every home, so instead we obtained data from the U.S. Census Bureau's American Community Survey for census tracts in 2019.