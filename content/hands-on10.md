---
layout: default
title: 10. Heatmaps
nav_order: 10
parent: Additional Content
---

# Heatmaps
Heatmaps are useful to show intensity or frequency of occurrence. Heatmaps can be thought about as generalized dot density maps. 

![heat map](./images/chestnut-heatmap.jpeg)

---

## Making a heatmap
*1*{: .circle .circle-yellow} Add the layer `chestnut-trees.geojson` from the thematic mapping subfolder to your QGIS project. 

<img src="./images/heatmap-layer_20251102.png" style="width:100%">

As it is, this is a dot density map. Now let's make it into a heatmap to accentuate areas where there are more chestnut street trees.

<br>

*2*{: .circle .circle-yellow} Open the **Layer Properties** and go to **Symbology**. Change the symbolization to **Heatmap**. 

<br>

*3*{: .circle .circle-yellow} Choose an appropriate color ramp. Then, click on the color ramp itself in order to adjust Color 1. Set the Opacity of Color 1 to be 0. In other words, make the lighter/lower end of the color ramp totally transparent. This will ensure that areas that have no value are see-through, and don't hide the map. 

<img src="./images/heatmap-opacity_20251102.png" style="width:60%">

<br>

*3*{: .circle .circle-yellow} **Radius** has to do with how far around the points the color blurs. 8-12 works well. I also recommend adjusting the **Rendering Quality** all the way to ***Best***, otherwise, the heatmap becomes quite pixelated. 

<img src="./images/heatmap-symbology_20251102.png" style="width:100%">

<br>


<img src="./images/heatmap_20251102.png" style="width:100%">