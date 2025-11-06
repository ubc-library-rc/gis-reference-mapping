---
layout: default
title: 2. Project Set up
nav_order: 2
parent: Hands On
---
# Setting up a QGIS Project 
{: .no_toc}

To begin the **Hands-On** portion of this workshop, we will open and set up the **QGIS project**. This page will introduce you to the QGIS interface, and guide you through loading data, setting the project properties, managing your layers, and creating spatial bookmarks. 



<details open markdown="block">
  <summary>
    On this page:
  </summary>
  {: .text-delta }
 - TOC
{:toc}
</details>
----

## The interface at a glance

In your workshop folder, open the file called `reference-mapping-workshop_YOURNAME.qgz`. If you have successfully downloaded and installed QGIS on your computer, this file should open in the application. (If need be, click New Empty Project.)


![qgis project](./images/qgis-project_20250911.png)


- **Menus** At the very top of your screen you'll see menus which, when clicked on, expand to show many more options and even sub-menus. Notice that these menus are only visible when you've clicked into the QGIS application. Though you can drag the application interface around your screen, the menus stay at the top. If you click out of the QGIS application, the menu will disappear. These menus provide easy access to a variety of tools you'll use in your everyday mapping. Like any new interface, it may take some time to become familiar with what's stored where. 

- **Toolbars** - The toolbar is the area at the top of your QGIS application with all the icons. The toolbar actually contains multiple toolbars, which are groups of icons that, when clicked, allow you to navigate around your map canvas, make click-based selections, edit layer geometries, create spatial bookmarks, and much more. You can customize this area of your GUI to fit your needs, adding and removing sets of tools by clicking on the great area of the toolbar.

- **Browser and Layers Panel** - When you open the project prepared for you, you should see two panels on the left-hand side of your interface. The browser panel lets you easily navigate your file system for data and project files. Your layers panel displays your project’s data layers and provides access to configuration settings. If you ever accidentally close a Panel, you can open it again by going to the View menu at the top of your screen, down to Panels, and then selecting the ones you wish. You can also right-click anywhere in the toolbar’s greyspace and select the Panels and Toolbars you want to show or hide.

- **Status Bar** - The status bar displays current information about the map canvas, and allows you to make adjustments in the map’s scale and rotation.

- **Map Canvas or Map View** - Call it either one. This is where the map is displayed and updated as layers are loaded. You can zoom/pan the map canvas as well as select features and other operations. 

You can change the look and feel of your GUI, as well as adjust default settings from the menu **QGIS-LTR --> Preferences** or the menu **Settings --> Options.** To increase the size of icons and text on your interface, go to the **Settings** menu at the top of your screen and click on **Options**. Then, resize the dialogue box so you can see the drop-down for "icon size" and "font." Icon changes will happen as soon as you click OK. Changes in font size won't update until you quit and restart QGIS, so make sure you save your project now. 
   
---- 

## Loading Data 
Once you’ve gathered relevant data, the next step is to add it to a QGIS project. There are a couple ways to add data to your map canvas. 

- **Browser panel** From the Browser panel, likely docked to the left of your screen, expand the `Home` directory (aka folder) and navigate to your workshop data folder. Expand that folder to see the data inside, then double-click or drag and drop each file to add it to your project. Alternatively, you can add a **Favorite** connection in the Browser panel to save you the trouble of finding your data folder. To do this, click “Favorites” at the top of the Browser panel's list and connect the workshop data folder as a favorite directory. Make sure not to click *into*, merely select it. 
- **Data Source Manager** The Data Source Manager is the same sort of portal as the Browser, just in a separate dialogue box rather than a docked panel. You can open the Data Source Manager by double-clicking the 3 colorful squares icon in the Toolbar, or from the Layer menu at the top of your screen.
- **Layer menu** A third way to add layers to your map canvas is through the Layer menu at the top of your screen. Under Layer, navigate to **Add Layer** (it should be the third item down) and select Add Vector Layer... or Add Raster Layer.... This will open the same Data Source Manager dialogue box as before.
- **Drag and drop** files from your data folder directly onto your map canvas. This method is not recommended as it can easily lead to data disorganization. 

To Do
{: .label .label-green }
Add the layers to your map *in the following order*. 
1. `ne_50m_ocean.shp` (World Oceans at medium scale from Natural Earth)
2. `ne_50m_admin_0_countries.shp` (World Countries at medium scale from Natural Earth)
3. `lpr_000b16a_e.shp` (Canadian Provinces from Statistics Canada)
4. `ne_50m_lakes.shp` (World Lakes and Reservoirs at medium scale from Natural Earth)

If for any reason you weren't able to download the necessary data, those files will be in the `backup-data` folder. Just remember to unzip them.
 

<!-- ![data added](./images/data-added_20250915.png) -->
![data added](./images/data-added2_20250915.png)

Zoom-in to Canada. The symbology, or coloring of each layer, is random. We will change these in the next section.

Now add `native-land-territories.geojson` (Indigenous territories downloaded from Native Land Digital using their API).  Your map canvas should look something like this now. 

<img src="./images/canada-zoom1-WGS84_20250915.png" style="width:49%">
<img src="./images/canada-zoom2-WGS84_20250915.png" style="width:49%">





 Your data isn't saved _inside_ your QGIS project. Rather, the *filepath connections* are saved, as well as any modifications to symbology made to the layers in QGIS. When mapping in QGIS, it's important to keep track of where the data you're working with is stored. If you move your data, QGIS won't know where to look for it and a red exclamation mark will appear in the Layers Panel. You can click on this warning to tell QGIS where the data is now stored. 
{: .note}


 

----

## Project Properties
You can access the Project Properties from the the **Project** menu. Open the Project Properties and click down to **CRS**. CRS stands for Coordinate Reference System, and describes the mathematics behind transforming a 3-dimensional Earth to fit on a 2-dimensional screen. A projection is part of the Coordinate Reference System, and is responsible for projecting a set of points from a 3-dimensional space onto a 2-dimensional plane. There are a variety of projections, each one preserving some characteristics of shape, area, distance, and direction, while distorting others. When choosing the best projection for your map, it is important to consider the content you are visualizing and the extent of the geographic area. Every spatial data layer comes with its own stored projection, often noted at the point of download. Note: If you don't set a projection at the start, your QGIS project will assume the projection of the first layer you add. 

To Do
{: .label .label-green }

For today's workshop mapping Canada, we will use the CRS: `NAD83 / Statistics Canada Lambert`. This will preserve direction and shape which is important as we are mapping a large geographic area that is quite close to the north pole. You can try different projections to see how they change the map, but be sure to set your project CRS to `NAD83 / Statistics Canada Lambert` in the end. 

![projection](./images/project-properties_20250915.png)
    

You'll notice setting the project projection changes how the layers are rendered.

<img src="./images/canada-zoom-NAD83Lambert_20250915.png" style="width:100%">


Setting the project CRS doesn’t change the stored projection of each layer, only how they are rendered ‘on the fly’ by QGIS. QGIS will reproject all the project layers ‘on the fly’ to match the project CRS. You can change the stored projection of layers with the Warp and Reproject Layer tools.

For more on Coordinate Reference Systems, see [here](https://ubc-library-rc.github.io/gis-georeferencing/content/projections.html) or check out our resource on [Understanding Map Projections](https://ubc-library-rc.github.io/map-projections/) for more. QGIS also has extensive documentation on [coordinate reference systems](https://docs.qgis.org/3.40/en/docs/gentle_gis_introduction/coordinate_reference_systems.html), and [pbcGIS](https://www.pbcgis.com/projection_fundamentals/) offers more background information if you're curious.
{: .note}




----

## Managing Layers
Although this workshop works with only a handful of layers, some projects require you to juggle more than 10 layers. Having strategies to stay organized is therefore important. Additionally, layers that cover the entire earth are quite large and require lots of processing power to load anew each time you pan and zoom around your map canvas. Best practice is therefore to "hide" or "turn off" layers you aren't using so as not to slow your computer down. Below are some tips to stay organized.

- **Rendering order** Note that we added layers to our project in a very specific order. This is because QGIS will render layers from the top down, meaning the layers to the top of your Layers Panel list will sit above the layers below. We added provinces and then lakes so that provinces could be seen above countries, and lakes above provinces. You can reorder your layers at any time by dragging them up or down. 

- **Turning layers on and off** Turn layers on and off (or hide and show them) by clicking the little checkbox beside each layer. If you've added a layer but don't see it rendered, it is likely underneath another layer. Rather than rearranging every layer until you find it, you can successively turn each layer off until you find the one you're looking for.  

- **Zoom to layer** To zoom to a layer, simply right-click (control-click) any layer and select the top option to "Zoom to Layer(s)". <img src="./images/zoom-to-layers_20250915.png" style="width:22%"> Zooming to a layer simply centers the extent of that layer in your map canvas. Often times when you first open a QGIS project, even if data is loaded and turned on, your map canvas will appear blank. Zooming to a layer will immediately populate your screen with the loaded layers. If you zoom to any of the global layers, you will return to the global view. 

     > Try zooming to `lpr_000b16a_e` (Canadian Provinces).  

- **Renaming layers** You can rename layers in the Layers Panel. This does not change the datasets themselves, but rather their nicknames as they appear in your QGIS project. To rename a layer, simply right-click the layer in your Layers Panel and go to "Rename Layer". 

  
     > Try renaming your layers. For example, rename `lpr_000b16a_e` to   `Provinces`. 


- **Grouping Layers** If you're ever working with numerous layers, you can create layer groups through the group icon <img src="./images/add-group-icon_20250915.png" style="width:4%"> or by right-clicking anywhere that's empty in the Layers Panel and selecting "Add Group". Once you've added and named a group, you can drag layers into it. You can move layers out of a group at any time, and right-click the group to remove or rename it. Each layers group will have its own visibility checkbox, meaning that even as you set the visibility for each individual layer within the group, only by rendering the group itself visible will any of its nested layers appear on your screen. 
   
     > Turn off the visibility of `native-land-territories` for the time being. 

- **Removing layers** Just as you can add layers to your QGIS project, you can remove layers at any time. This will not delete the datasets themselves; after all, they are not saved inside your QGIS project (as ArcGIS would do). Rather, it is the file connections that are saved, as well as edits to their symbology made in QGIS. To remove a layer connection from your project, simply right-click that layer in your Layers Panel and select "Remove Layer...". 

- **Checking file paths** If you are ever uncertain where a loaded layer is stored on your physical computer, hover over the layer to see its file path.

- **Refreshing Data Source** If you add new data to your working folder already pinned as a favorite directory in your Browser Panel, you might need to "Refresh" the folder connection for the new files to appear. Simply right-click the folder connection and select "Refresh". You can also click the Refresh icon <img src="./images/refresh-icon_20250915.png" style="width:4%"> to refresh all connections. 


- **Exporting Layers** Exporting a layer essentially makes a copy of the dataset on your computer with a name, file type, and location of your choice. This can be useful if you want to make a copy of a layer, save a temporary layer as a permanent file, or save a selection as a new layer/dataset. To export a layer, simply right-click the layer, go to "Export" --> "Save Feature As...". Note that your new file will not have the same symbology, though you can copy/paste one layer's symbology to another. "Duplicating" a layer, which you can also do by right-clicking a layer in your Layers Panel, doesn't create a copy of the dataset, just adds it twice to your project. 

- **Copy/Paste Symbology** Right-click the layer whose symbology you want to copy in the Layers Panel, go to "Styles" --> "Copy Style" --> "Symbology". Then right-click the target layer, and go to "Styles" --> "Paste Style" --> "Symbology".


<!-- - **Managing data from browser panel** Note that you _can_ delete data on your computer from the Browser Panel by right-clicking the layer  (deleting files) -->


## Spatial Bookmarks
Another tip, especially if you're using a single layer to make a map of different locations, is to make **spatial bookmarks**. A spatial bookmark is exactly what it sounds like: a way to bookmark a canvas extent to return to layer. You can add a spatial bookmark from the bookmark icon in the **Toolbar**, from the **View menu**, or from the Spatial Bookmark tab in your **Browser Panel**. by going to here or there. You can then set it to your map canvas, or a layer, etc. You can then save the bookmark with a name to your project (this project alone) or to your user settings (every QGIS project you ever make and open). 

![spatial bookmark](./images/spatial-bookmark_20250915.png)


To Do
{: .label .label-green }

Make a spatial bookmark of Canada. If you've already zoomed to the provinces layer, set your spatial bookmark extent to "Map Canvas Extent". Otherwise, be sure Canada is centered on your screen first, or set the provinces layer as your extent. Save to Project Bookmarks. 


<img src="./images/spatial-bookmark-parameters_20250915.png" style="width:70%">

<br>

You are now setup to begin mapping! Be sure to **SAVE YOUR PROJECT** before continuing on. Save from either the save icon in your toolbar or from the Project menu --> Save. 









