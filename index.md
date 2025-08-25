---
layout: default
title: Introduction
nav_order: 1
has_children: true
---

This workshop is in development and not yet complete.
{: .note}

# Mapping for Academic Publication

This workshop will provide an overview of how to create simple, static maps to accompany academic publications. We will use [QGIS](https://qgis.org/), a free and open-source Geographic Information System (GIS) for analyzing, modifying, and visualizing spatial data. This workshop is geared towards mapping novices who either want to create a map that geographically contextualizes their study area, or whose project involves data with a spatial component they are eager to visualize. While making such maps on your own can feel daunting, this workshop aims to give participants the confidence to: 

- Decide what kind of map best conveys their research or contextualizes their study; 
- If needed, find and download relevant spatial data; 
- Upload datasets into QGIS, as well as edit and symbolize data layers;
- Compose a map layout that includes a title, scale bar, legend, and north arrow; and
- Export this map into formats compatible for print and digital publication.

<!-- The maps you will learn to create through this workshop are quite basic. For example, contextual location or basemap with simple data layer. (show examples below in side-by-side; maybe one with data points or polygon, one with satellite basemap?) If you are interested in more advanced spatial analysis, check out xyz workshops. For webmapping/making dynamic and interactive maps, check out webmapping workshop. If you are unsure the output you want, look through our Telling Spatial Stories workshop/resource base to get oriented.// project design guidance.  -->
 

## Audience

**Geospatial novices welcome!** No prior experience with mapping is necessary, though familiarity with QGIS is helpful. You are encouraged to explore our workshops [Intro to QGIS](https://ubc-library-rc.github.io/gis-intro-qgis/), [Tools and Workflows in QGIS](https://ubc-library-rc.github.io/gis-tools-workflows/), and [Plugins in QGIS](https://ubc-library-rc.github.io/gis-plugins-qgis/) *in that order* for a gentle introduction.  

If your goal is to map your research area or  want to map your research area, or show your data points on a basemap, this workshop is for you. However, if you are looking to conduct more advanced spatial analysis on your data, we recommend the QGIS workshops listed above. If you realize you actually want to make interactive and dynamic web-based maps that can be embedded in a website or shared via a link, check out our [Webmapping Workshop](https://ubc-library-rc.github.io/gis-intro-leaflet/).
Finally, if you don't know what kind of output you want just yet, we encourage you to explore our resource for [Telling Spatial Stories](https://ubc-library-rc.github.io/gis-spatial-stories/). Here, you will be guided through choosing an output format and tools that serve your purpose, skillset, and timeframe. 



## Before the Workshop

1.  **Download QGIS!** QGIS can be downloaded from [qgis.org's Downloads page](https://qgis.org/en/site/forusers/download.html). In most cases, you'll want to download and install the **Long term release** instead of the latest release - currently **QGIS 3.40.4 'Bratislava'**. This will give you most of the functionality you'll need, without encountering the software bugs of newly released versions. See the subpage to this page, **[installing QGIS,](./installing-qgis.md), for further guidance.**


2.   **Download and unzip** the workshop data folder below. Download it to a folder on your physical computer, such as Desktop or Downloads, *not* OneDrive.
<!-- This folder contains... Why its prepared for participants...   -->

[Download Workshop Data](reference-mapping-workshop.zip){: .btn .btn-blue }


If you're coming to this workshop with your own data in-hand, be sure to move it inside the unzipped workshop data folder. Additionally, make sure it is either in a spatial data format (such as Esri Shapefile, `.shp`, or geoJSON, `.geojson`), or saved as a `.csv`. For the purposes of this workshop, your dataset must have coordinate information saved in two separate columns, one for latitude and one for longitude. If you only have cities/countries or street addresses, follow the link in the resources below to book a 1:1 consult for additional support. If you have street addresses, you can also *geocode* these in QGIS (see [here](https://ubc-library-rc.github.io/gis-plugins-qgis/content/geocoding.html) for documentation.)
{: .note}
      

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