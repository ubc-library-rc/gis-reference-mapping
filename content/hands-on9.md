---
layout: default
title: 9. Proportional Symbol Maps
nav_order: 9
parent: Additional Content
---
# Thematic Mapping - Proportional Symbol Maps

Proportional symbol maps are useful to visualize the quantity of something across respective locations. Choropleth maps use a color gradient to convey value differentials, whereas proportional symbol maps use symbol size. Proportional symbols are quite intuitive, and can be combined with other parameters like color and lettering size to provide rich spatial information. Proportional symbols can even be layered atop a choropleth map. See [Axis Maps](https://www.axismaps.com/guide/proportional-symbols) for a guide to proportional symbol maps. 

Note: In most cases you *do not* normalize values when using proportional symbols, as that would reduce the range in difference. If anything, it can be useful to exaggerate the range slightly. While Absolute Scaling renders symbols increasingly larger along a linear scale, Perceptual/Apparent Scaling compensates for the eye's tendency to reduce difference in sizes close together. [See here for more](https://makingmaps.net/2007/08/28/perceptual-scaling-of-map-symbols/). 

![prop symbol map](./images/chestnut-proportional-symbol.jpeg)

<!-- https://schoolofcities.github.io/urban-data-storytelling/urban-data-visualization/proportional-symbol-maps/proportional-symbol-maps.html -->

----

## Making a proportional symbol map in

You can make proportional symbol maps in QGIS simply by converting polygons to centroids (if not already points) and then going to symbology and choosing Graduated. Alternatively, if you want to spend extensive time styling your map and proportional symbols manually, you can export centroids (and other geographic layers) as an `.svg` file and open it in an illustration software like Adobe Illustrator or [Inkscape](https://inkscape.org/). The formula for *radius* of proportional symbols in absolute scaling is as follows: 
> r<sub>C</sub> = (v<sub>C</sub> / v<sub>L</sub>) <sup>0.5</sup> * r<sub>L</sub>
<br>

> where r<sub>C</sub> is the radius of the circle to be calculated,<br>
> r<sub>L</sub> is the radius of the largest circle,<br>
> v<sub>C</sub> is the data value of the circle to be calculated, and<br>
> v<sub>L</sub> is the data value of the largest circle<br>

For perceptual scaling, increase the exponent to 0.57.   

Note: The language for this formula is from GEOS372 Cartography Lab 6 by Dawn Mooney. 

---- 