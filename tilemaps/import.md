---
layout: default
---

[Home](../) / [Tile Maps](./index.html) / Import a Tile Map

## Import a Tile Map
On this guide we will go over the steps to importing a tile map from Tiled to Unreal Engine as well as some tips and tricks to make the process easier.

[Quick Video Guide](https://www.youtube.com/watch?v=AQnpu9husAo)

**1.-** The first step is to create a Tile Set in Tiled to be able to use it in our Tile Map (you can skip this step if you want to embed the Tile Set into the Tile Map). Refer to the [Import a Tile Set](../tilesets/import.html) guide for more information.

**Note:** The plugin supports both embedded Tile Sets (which lives inside the Tile Map) or standalone Tile Sets (in a sepparate file). My recommendation is to use standalone Tile Sets, so you can reuse them in different maps.

**2.-** Once you have the Tile Set ready, we can proceed and create a Tile Map in Tiled and save it. At this time, the plugin only supports the **tmj** and **json** file extensions.

**Note:** The tile map file should be placed within the Content folder of your project in order to allow moving the project around and use the reimport feature. I recommend placing your files in a folder like `<Project Folder>/Content/Maps/<YourMapFolder>/<YourMap>.json`

**3.-** Finally, to import the map to Unreal Engine, click the `Import` button on the plugin UI and follow the instructions. It will ask the file to import, where you should select the previously created Tile Map, and where to place the uasset file within the Content folder. I recommend placing the imported file in the same folder as the Tiled file.

**Note:** You can set up some Unreal Engine properties on the tile map (such as `Pixels Per Unreal Unit` or `Separation Per Layer`) from Tiled and will get automatically set up when importing. Check out the [Custom Properties](./custom-properties.html) for more information.

## Reimport a Tile Map
If at some point you make changes to the Tile Map in Tiled and you want to bring them over to Unreal Engine, is just as easy as clicking `Reimport` on the plugin UI. 

Alternatively, you can automate the process by enabling the `Auto Reimport` feature, which will reimport the asset when it detects any changes.

## Delete an imported Tile Map
To delete an imported Tile Map, click on the `Delete` button in the plugin UI and it will delete the Tile Map and any embedded Tile Sets that were imported with it.

**Note:** Do not try to delete the files imported to Unreal Engine manually, as it will cause issues with the plugin. Always use the plugin UI to manage the imported files.