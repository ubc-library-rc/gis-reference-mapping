---
layout: default
title: 13. Cartograms
nav_order: 13
parent: Additional Content
---
# Thematic Mapping - Cartograms

Cartograms distort area to emphasize the value associated with a geographic region. When using cartograms, it's important to consider whether your audience is already familiar with the un-distorted  geography, otherwise they might not glean the added information. 
![cartogram map](./images/chestnut-cartogram-map.jpeg)

----

## Making a cartogram
Turn back on the `chestnut-count` layer. In order to create a cartogram, we need to install a **plugin**. [QGIS plugins](https://plugins.qgis.org/) are user developed tools that extend QGIS functionality beyond the basics. Explore our workshops on [plugins in QGIS](https://ubc-library-rc.github.io/gis-plugins-qgis/) for more. 

<!-- <img src="./images/plugin-screen1_20250319.png" style="width:80%"> -->

*1*{: .circle .circle-yellow}  Plugins can be downloaded directly from the web, or from within the QGIS interface. To download plugins from within the QGIS interface, click on the **Plugin** menu at the top of your screen and select **Manage and Install Plugins...**. Go down to Settings and ensure you are including Experimental Plugins in your search.

<img src="./images/cartogram-install-plugin_20251102.png" style="width:80%"> 

The plugin we will install is called `cartogram3`. Search for it and then click **Install**. 
 
<img src="./images/cartogram-plugin_20251102.png" style="width:80%"> 

<!-- When you download plugins, they will show up as additional tools in your menu drop downs as well as toolbox. If you can't find a plugin, you can always search it by name in the **Help** menu. You only have to install plugins once. However, sporadically you will get a notification upon opening QGIS to update a plugin. You can update any plugin by simply searching it in the Plugins Manager and following the button prompts. If you ever install a new version of QGIS, you *will* have to re-install your plugins. 
{: .note} -->

<br>

*2*{: .circle .circle-yellow} Your newly installed cartogram plugin should now show up under the **Vector Tool** menu at the top of your screen.

<img src="./images/cartogram-compute_20251102.png" style="width:100%">

<br>

*3*{: .circle .circle-yellow} Set `chestnut-count` as the Input Layer, and select `chestnut-trees` as the Field. Then run the tool.

<img src="./images/cartogram-parameters_20251102.png" style="width:60%">

<img src="./images/cartogram_20251102.png" style="width:80%">

