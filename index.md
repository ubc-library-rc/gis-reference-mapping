---
layout: default
title: Introduction
nav_order: 1
has_children: true
---
# Reference Mapping for Academic Publication
<br>
    

This workshop will provide an overview of how to create simple, static reference maps for academic publication. By the end of this workshop, participants will be able to:

- Find and download spatial data to serve as geographic context
- Upload datasets into QGIS, a free and open-source geographic information system for analyzing, modifying, and visualizing spatial data
- Format and symbolize spatial data layers, and compose a map for print that includes a title, scale bar, legend, and north arrow
- Export map into  formats compatible for print and web publication

The maps you will learn to create through this workshop are very basic. For example, contextual location or basemap with simple data layer. (show examples below in side-by-side)
 <!-- maybe one with data points or polygon, one with satellite basemap?  -->

## Audience

**Geospatial novices welcome!** No prior experience with mapping is necessary, though familiarity with QGIS may be helpful. Check out our workshops [Intro to QGIS](https://ubc-library-rc.github.io/gis-intro-qgis/), [Tools and Workflows in QGIS](https://ubc-library-rc.github.io/gis-tools-workflows/), and [Plugins in QGIS](https://ubc-library-rc.github.io/gis-plugins-qgis/) in that order for a gentle introduction.  

If you want to map your research area, or show your data points on a basemap, this workshop is for you. However, if you are looking to conduct spatial analysis on your data, recommend the workshops listed above. Finally, if you don't know what kind of output you want just yet, we encourage you to explore our resource for [Telling Spatial Stories](https://ubc-library-rc.github.io/gis-spatial-stories/). Here, you will be guided through choosing an output format and tools that serve your purpose, skillset, and timeframe. 


## Before the Workshop

1.  **Download QGIS!** QGIS can be downloaded from [qgis.org's Downloads page](https://qgis.org/en/site/forusers/download.html). In most cases, you'll want to download and install the **Long term release** instead of the latest release - currently **QGIS 3.40.4 'Bratislava'**. This will give you most of the functionality you'll need, without encountering the software bugs of newly released versions. **[See the subpage, installing QGIS,](./installing-qgis.md) for further guidance.**


2.   **Download and unzip** the workshop data folder below. This folder contains... Why its prepared for participants...  
[Download Workshop Data](reference-mapping-workshop.zip){: .btn .btn-blue }


If you have your own data you want to map, move it inside the unzipped data folder. Additionally, make sure it is either in a spatial data format (such as Esri Shapefile, `.shp`, or geoJSON, `.geojson`), or saved as a `.csv`. For the purposes of this workshop, your dataset must have coordinate information saved in two separate columns, one for latitude and one for longitude. If you only have cities/countries or street addresses, follow the link in the resources below to book a 1:1 consult for additional support. If you have street addresses, you can also *geocode* these in QGIS (see [here](https://ubc-library-rc.github.io/gis-plugins-qgis/content/geocoding.html) for documentation.)

      

<br>


--- 

#### GIS Resources at UBC:
- General Informational website for all things UBC GIS: [gis.ubc.ca](http://gis.ubc.ca/)
- UBC Library's guide for finding and working with GIS resources: [guides.library.ubc.ca/gis](http://guides.library.ubc.ca/gis)
- Archive of all [Research Commons workshops](https://ubc-library-rc.github.io/)
- Research Commons [Events Calender](https://researchcommons.library.ubc.ca/workshops/) for upcoming facilitated workshops
- Contact UBC Library’s Geospatial team: `library.gis@ubc.ca`
- Schedule a 1:1 consult with the geospatial team [here](https://libcal.library.ubc.ca/appointments/research_commons#s-lc-public-pt)


<p style="margin-top:90px"></p>
<p style="color:grey; font-size:13px">This workshop was authored by <a href="https://geog.ubc.ca/profile/lily-crandall-oral/" target="_blank">Lily Demet</a> and reviewed by Alex Alisauskas.</p>