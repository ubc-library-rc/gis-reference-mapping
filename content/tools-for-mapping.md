---
layout: default
title: Tools for Mapping
nav_order: 3
has_children: true
---
# Mapping Tools 
There are many tools for mapping suited to a range of skillsets. Today's workshop will use QGIS — a free and open source Geographic Information System (GIS) — to visualize spatial data and make simple, static maps as one might for academic publication.  GIS isn't the only way to make a reference map. However, it provides ample detail and involves your original work. For a comprehensive list of different mapping tools and software, see [here](https://ubc-library-rc.github.io/gis-spatial-stories/content/resources-static-maps.html). QGIS, the GIS application we will use, is quite beginner friendly, especially if you want to just make a simple reference map. And, if you do decide to do more complex spatial analysis, you're halfway there. 

If you're interested in spending more time honing the aesthetics of your map, you can always export a rudimentary map from QGIs and conduct advanced editing in a graphics illustration software such as Adobe Illustrator or its open-source alternative, [Inkscape](https://inkscape.org/).


### Static or dynamic
While outside the remit of this workshop, may be important to you is whether your map is static or dynamic. Both reference maps and thematic maps can be either static or dynamic. Static maps tell a spatial story at a single scale. Static maps can be exported/stored/formatted as an image (.jpeg or .png), can be exported as a pdf, printed or embedded digitally into website or online publication. They can also be included in an academic paper, poster, or flyer. Dynamic maps, on the other hand, allow the user to interact with your spatial story. Dynamic display data in an interactive fashion, allowing viewers to pan around and zoom in and out to reveal more information at different scales. This workshop focuses on static reference maps. If you're interested in webmapping, our resources for [webmapping with QGIS Plugins](https://ubc-library-rc.github.io/gis-plugins-qgis/content/webmapping.html) workshop, [webmapping with Leaflet](https://ubc-library-rc.github.io/gis-intro-leaflet/), and our[overview of webmapping tools](https://ubc-library-rc.github.io/gis-spatial-stories/content/resources-web-mapping.html).

 

- maybe include walk through for exporting into inkscape, or links to resources
- maybe include some more tools?

## Geographic Information Systems (GIS) 
This workshop uses a Geographic Information System (GIS) to generate reference maps for publication. GIS is an abbreviation for Geographic Information System. A nice description of GIS that provides a bit of relevancy comes from QGIS's [*A Gentle Introduction to GIS*](https://docs.qgis.org/3.10/en/docs/gentle_gis_introduction/introducing_gis.html):

  >*Just as we use a word processor to write documents and deal with words on a computer, we can use a GIS application to deal with spatial information on a computer*

With that in mind, there are 3 main forms of GISs:
1. **Utilities and Services (tasks)** - Scripts and programming libraries that manipulate spatial data in specific ways. For example, [**geocoding**](https://desktop.arcgis.com/en/arcmap/latest/manage-data/geocoding/what-is-geocoding.htm) services geolocate a set of points based on address or coordinate attribute data. [MMQGIS](https://plugins.qgis.org/plugins/mmqgis/) is a QGIS plugin which contains a tool for geocoding. 

2. **Desktop (analyses)** - Software that provides a suite of tools for processing and spatially analyzing data. In other words, GIS applications you interact with through a graphical user interface from a computer. Examples include the QGIS desktop app we will use today and Esri ArcGIS Pro. 

3. **Infrastructure (management)** - Server and web resources that manage, curate, and distribute collections of spatial data. While Esri offers Server web services with ArcGIS Online, many [open source GIS servers](https://mapscaping.com/open-source-gis-servers/) are out there. 

