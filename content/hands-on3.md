---
layout: default
title: 3. Modifying Layers
nav_order: 3
parent: Hands On
---
# Modifying Layers
{: .no_toc}

As they are, the layers we've added to our map canvas aren't particularly aesthetic, nor is foreground adequately differentiated from background. This page (and the next) will guide you through modifying your layers' symbology to create a more polished looking map where what's deemed important stands out. 

This page will also note some considerations specific to mapping for academic publication. 



<details open markdown="block">
  <summary>
    On this page:
  </summary>
  {: .text-delta }
 - TOC
{:toc}
</details>
----


## Attribute Table
The **Attribute Table** contains the tabular data associated with a layer. Though not relevant to today's focus on reference mapping, it is important you know what the attribute table is, and how to access it. To open a layer's attribute table, right-click the layer in the Layers Panel and go to "Open Attribute Table". For more experience in with the attribute table, you are encouraged to explore our [Intro to QGIS](https://ubc-library-rc.github.io/gis-intro-qgis/) and [Tools and Workflows in QGIS](https://ubc-library-rc.github.io/gis-tools-workflows/) beginner workshops.

To Do
{: .label .label-green }
Open the attribute table of the `Provinces` layer. 
Note that there are several attributes (columns) that describe each feature (row) in this dataset. Manually re-size the column widths until you can read each attribute.

<img src="./images/attribute-table_20250915.png" style="width:90%">


## Layer Properties 
{: .no_toc}
Just as the QGIS Project had Project Properties, each layer has properties of its own. To view a layer's properties, right-click the layer in the Layers Panel and go to "Properties..." at the bottom. We won't dwell on all the project properties today, but notice you can learn more information about the layer here, including where it's stored on your computer, and its projection. 


## Labelling 
Two project properties we _will_ concern ourselves with are **Labels** and **Symbology**. Labels allow you to add labels to a layer based on an attribute value. You can turn off the labels at any time by returning to a layer's properties, or by right-clicking the layer and clicking "Show Labels" again. 

To Do
{: .label .label-green }
Add provincial labels based on `PRENAME`. You can customize your labels by increasing the text size, adding a buffer, or changing the label placement. 

<img src="./images/add-labels_20250915.png" style="width:100%">
<img src="./images/labels-added_20250915.png" style="width:100%">



## Symbology
The other important layer property for reference mapping is Symbology. Symbology governs the outline and color fill of points, lines, and polygons. The symbology style for any given vector layer can be Single, Categorized, Graduated, etc. For now, let's stick with Single. This means that each layer will have a single symbology, or color/outline. 

Depending on the audience and publisher of your reference map, you might have constraints such as Black and White. Keep this in mind. For now, we'll map in color.

To Do
{: .label .label-green }
Change the color of the ocean.

1. Right-click the ocean layer and go to Properties --> Symbology. 
2. Click down to Simple Fill. 
3. Click on the color bar to change the color. Expand the dialogue window if necessary. 
4. You can also change the "stroke", or outline color, or, by setting Stroke style to "No line", remove it all together. 

<img src="./images/symbology_20250915.png" style="width:90%">

 If you want to make your map in Black & White, change the Color Model from RGB to CYMK. Then set everything but K to 0. You can also color sample from the eye-dropper tab. 

<img src="./images/changing-color_20250915.png" style="width:65%">


### Categorized Symbology
{: .no_toc}
Imagine you had a polygon layer with multiple features, such as provinces in Canada or Indigenous territories, and you wanted each province or territory to be distinguished by its own color. In this case, you'd want to change the symbology type from Single Symbol to Categorized. 

To Do
{: .label .label-green } 
Change the symbology for the Native Land dataset. 

<img src="./images/native-land-territories-symbology_20250915.png" style="width:100%">

Currently, each territory has a random color. You can click each color square beside the province to individually change its color. We won't attempt this, however, as there are too many features. Decreasing the layer's opacity (aka increasing its transparency) will allow the provinces or landforms to be seen beneath it. Try hiding the provinces for a moment. 

<img src="./images/native-land-territories-categorized-symbology_20250915.png" style="width:100%">

Notice, however, that transparent or not, the territories from the Native Land dataset do not appear to overlap. However, when referencing the original map, [native-land.ca](https://native-land.ca/), we see much overlap in the boundaries. In order to show this in our QGIS project, we have to adjust the symbology for each territory. If you remember, there were a lot! Luckily, we can do a sort of select-all to edit them all at once.

Select the first territory listed. Holding the Shift key of your computer down, scroll to the bottom and select the last territory. This should highlight the whole list. 

<img src="./images/selecting-all_20250915.png" style="width:100%">

Then, click on "Symbol". On "Fill", decrease the opacity to around 60%. Then click "OK". Click "Apply" from symbology window to see the results on your map canvas. There should now be significant overlap. Click "OK" to close the symbology window. Save your project. 

<img src="./images/overlap-zoomed-out_20250915.png" style="width:100%">

Turn on labels for Indigenous territories, and zoom to the Vancouver area. 

<img src="./images/overlap-zoomed-in_20250915.png" style="width:100%">




<br>
Now you know how to change the symbology of a layer, either symbolizing all polygons the same color, or giving them each a unique color. If you wanted each province to have a different color, change the symbology from "Single Symbol" to "Categorized". Choose `PRENAME` as the value. Then click "Classify"

Currently, they are all random colors. You can click each color square beside the province to individually change its color. Just like we practiced above, to edit all at once (for instance to remove the outlines of all provinces) hold the Shift key down as you select Alberta to Yukon, then click on "Symbol" at the top. Go down to "Simple Fill" and set the "Stroke style" to "No Line". Hit Apply in the main Symbology dialogue window to view the results.

<img src="./images/classify-provinces-categorized-symbology_20250915.png" style="width:100%">

<img src="./images/categorized-symbology_20250915.png" style="width:100%"> 

<Br>

Before changing any more symbology, let's talk about **Visual Hierarchy**. 

