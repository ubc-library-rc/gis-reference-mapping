---
layout: default
title: Introduction
nav_order: 1
has_children: true
---

This workshop is in development and not yet complete.
{: .note}

# Reference Mapping for Academic Publication

This workshop will provide an overview of how to create simple, static maps to accompany academic publications. We will use [QGIS](https://qgis.org/), a free and open-source Geographic Information System (GIS) for analyzing, modifying, and visualizing spatial data. This workshop is geared towards mapping novices who either want to create a map that geographically contextualizes their study area, or whose project involves data with a spatial component they are eager to visualize. While making such maps on your own can feel daunting, this workshop aims to give participants the confidence to:

- Decide what kind of map best conveys your research or contextualizes your study;
- If needed, find and download relevant spatial data;
- Upload datasets into QGIS, as well as edit and symbolize data layers;
- Compose a map layout that includes a title, scale bar, legend, and north arrow; and
- Export this map into formats compatible for print and digital publication.

<!--

![canada map](./content/images/canada-map-demo.jpeg)
![canada map](./content/images/canada-map-multicolored.jpeg)

![native land map](./content/images/native-land-map.jpeg) -->

<!--carousel styling and code from W3schools-->
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
* {box-sizing: border-box}
body {font-family: Verdana, sans-serif; margin:0}
.mySlides {display: none}
img {vertical-align: middle;}
.slideshow-container {
max-width: 1000px;
position: relative;
margin: auto;
}
.prev, .next {
cursor: pointer;
position: absolute;
top: 50%;
width: auto;
padding: 16px;
margin-top: -22px;
color: black;
background-color: rgba(255, 255, 255, 0.51);
font-weight: bold;
font-size: 18px;
transition: 0.6s ease;
border-radius: 0 3px 3px 0;
user-select: none;
}
.next {
right: 0;
border-radius: 3px 0 0 3px;
}
.prev:hover, .next:hover {
background-color: rgba(142, 122, 163, 0.5);
}
.text {
color: #f2f2f2;
font-size: 15px;
padding: 8px 12px;
position: absolute;
bottom: 8px;
width: 100%;
text-align: center;
}
.numbertext {
color: #211c1cff;
font-size: 12px;
padding: 8px 12px;
position: absolute;
top: 0;
}
.dot {
cursor: pointer;
height: 10px;
width: 10px;
margin: 0 2px;
background-color: #bbb;
border-radius: 5%;
display: inline-block;
transition: background-color 0.6s ease;
}
.active, .dot:hover {
background-color: #717171;
}
.fade {
animation-name: fade;
animation-duration: 1.5s;
}
@keyframes fade {
from {opacity: .4}
to {opacity: 1}
}
@media only screen and (max-width: 300px) {
.prev, .next,.text {font-size: 11px}
}
</style>
</head>

<body>
<div class="slideshow-container">
<div class="mySlides fade">
  <div class="numbertext">1 / 3</div>
  <img src="./content/images/canada-map-demo.jpeg" style="width:100%">
  <!-- <div class="text">Caption Text</div> -->
</div>
<div class="mySlides fade">
  <div class="numbertext">2 / 3</div>
  <img src="./content/images/canada-map-multicolor.jpeg" style="width:100%">
</div>
<div class="mySlides fade">
  <div class="numbertext">3 / 3</div>
  <img src="./content/images/native-land-map.jpeg" style="width:100%">
</div>
<a class="prev" onclick="plusSlides(-1)">❮</a>
<a class="next" onclick="plusSlides(1)">❯</a>
</div>
<div style="text-align:center">
  <span class="dot" onclick="currentSlide(1)"></span> 
  <span class="dot" onclick="currentSlide(2)"></span> 
  <span class="dot" onclick="currentSlide(3)"></span> 
</div>
<script>
let slideIndex = 1;
showSlides(slideIndex);
function plusSlides(n) {
  showSlides(slideIndex += n);
}
function currentSlide(n) {
  showSlides(slideIndex = n);
}
function showSlides(n) {
  let i;
  let slides = document.getElementsByClassName("mySlides");
  let dots = document.getElementsByClassName("dot");
  if (n > slides.length) {slideIndex = 1}    
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";  
  }
  for (i = 0; i < dots.length; i++) {
    dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";  
  dots[slideIndex-1].className += " active";
}
</script>
</body>
</html>

---

## Audience

**Geospatial novices welcome!** No prior experience with mapping is necessary, though familiarity with QGIS is helpful. Before taking this workshop, you are encouraged to explore our [Intro to QGIS](https://ubc-library-rc.github.io/gis-intro-qgis/), [Tools and Workflows in QGIS](https://ubc-library-rc.github.io/gis-tools-workflows/), and [Plugins in QGIS](https://ubc-library-rc.github.io/gis-plugins-qgis/) offerings _in that order_ for a gentle introduction.

If your goal is to map your research area or want to map your research area, or show your data points on a basemap, this workshop is for you. However, if you are looking to conduct more advanced spatial analysis on your data, we recommend the QGIS workshops listed above. If you realize you actually want to make interactive and dynamic web-based maps that can be embedded in a website or shared via a link, check out our [Webmapping Workshop](https://ubc-library-rc.github.io/gis-intro-leaflet/).
Finally, if you don't know what kind of output you want just yet, we encourage you to explore our resource for [Telling Spatial Stories](https://ubc-library-rc.github.io/gis-spatial-stories/). Here, you will be guided through choosing an output format and tools that serve your purpose, skillset, and timeframe.

## Before the Workshop

1.  **Download QGIS!** QGIS can be downloaded from [qgis.org's Downloads page](https://qgis.org/en/site/forusers/download.html). In most cases, you'll want to download and install the **Long term release** instead of the latest release - currently **QGIS 3.40.4 'Bratislava'**. This will give you most of the functionality you'll need without encountering the software bugs of newly released versions. See the subpage to this page **[installing QGIS](./installing-qgis.md)** for further guidance.

2.  **Download and unzip** the workshop data folder below. Download it to a folder on your physical computer, such as Desktop or Downloads, _not_ OneDrive.

[Download Workshop Data](reference-mapping-workshop.zip){: .btn .btn-blue }

If you're coming to this workshop with your own data in-hand, be sure to move it inside the unzipped workshop data folder. Additionally, make sure it is either in a spatial data format (such as Esri Shapefile, `.shp`, or geoJSON, `.geojson`), or saved as a `.csv`. For the purposes of this workshop, your dataset must have coordinate information saved in two separate columns, one for latitude and one for longitude. If you only have cities/countries or street addresses, follow the link in the resources below to book a 1:1 consult for additional support. If you have street addresses, you can also _geocode_ these in QGIS (see [here](https://ubc-library-rc.github.io/gis-plugins-qgis/content/geocoding.html) for documentation.)
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
