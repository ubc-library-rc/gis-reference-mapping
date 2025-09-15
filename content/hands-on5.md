---
layout: default
title: 5. Basemaps (Optional)
nav_order: 5
parent: Hands On
---

# Basemaps
What they are and why use them. Include an Example map. 



## Adding basemaps from web plugin
While your out-of-the-box QGIS applicaiton will have a few basemap options under the XYZ tab of your Browser Panel, you can access way more with a plugin. [QGIS Plugins](https://plugins.qgis.org/) are user developed tools that extend QGIS functionality beyond the basics. There are two popular plugins for webmap libraries called QuickMapServices and OpenLayers.The following documentation will show you how to install the QuickMapServices plugin, add basemaps to your QGIS project, and create and export a map using one of them. 


### Install Plugin
[QGIS plugins](https://plugins.qgis.org/) are user developed tools that extend QGIS functionality beyond the basics. To access basemaps, we'll first install the QuickMapServices plugin. Click on the **Plugin** menu at the top of your screen and select **Manage and Install Plugins...**
![Install plugin](./images/)   

In the dialogue box that opens, select **All** as a search category on the left and type "QuickMapServices" as one word. Install the plugin and close the dialogue box.
![quick map services](./images/)

### Add Basemap
Now go to the **Web** menu at the top of your screen. You should see the QuickMapServices plugin. Hover over it and click "Settings" at the bottom of the menu that pops up. In the settings dialogue box go to the "More services" tab and click "Get contributed pack." Click **save** to close settings and return to the **Web** menu. This time when you hover over the QuickMapServices plugin you will see an array of basemap options. Select OpenStreetMap as your basemap. Like QGIS, [Open Street Map (OSM)](https://www.openstreetmap.org/about) is open source and user developed.   

Make sure to drag your basemap to the bottom in your Layers Panel. Remove the basemap at anytime by right clicking the layer and selecting "remove." 

![Add basemap](./images/)


If you find web-based maps interesting, check out the Research Commons' [Leaflet Workshop!](https://ubc-library-rc.github.io/gis-intro-leaflet/). If you find plugins compelling, check out our workshop on [Plugins in QGIS](https://ubc-library-rc.github.io/gis-plugins-qgis/).
{: .note}






## Making a map

Considerations. Then documentation. 

<img src="./images/ubc-campus-demo.jpeg" style="width:55%">

