---
layout: default
---

[Home](../) / [Tile Maps](./index.md) / Import a Tile Map

## Import a Tile Map
On this guide we will go over the steps to importing a tile map from Tiled to Unreal Engine as well as some tips and tricks to make the process easier.

[Quick Video Guide](https://www.youtube.com/watch?v=AQnpu9husAo)

**1.-** The first step is to create a [Tile Set](../tilesets/index.md) in Tiled to be able to use it in our Tile Map (you can skip this step if you want to embed the Tile Set into the Tile Map). Refer to the [Import a Tile Set](../tilesets/import.html) guide for more information.

**Note:** The plugin supports both embedded [Tile Sets](../tilesets/index.md) (which lives inside the Tile Map and will be imported with it) or standalone [Tile Sets](../tilesets/index.md) (in a sepparate file). It is recommended to use standalone [Tile Sets](../tilesets/index.md), so you can reuse them in different tile maps.

**2.-** Once you have the [Tile Sets](../tilesets/index.md) ready, we can proceed and create a Tile Map in Tiled and save it. At this time, the plugin only supports the **tmj** and **json** file extensions.

**Note:** The Tile Map file should be placed within the `Content` folder of your project in order to allow moving the project around and use the reimport feature. It is recommended to place your files in a folder structure like `<Project Folder>/Content/Maps/<YourMapFolder>/<YourMap>.json`

**3.-** Finally, to import the map to Unreal Engine, click the `Import` button on the plugin UI and follow the instructions. It will ask the file to import, where you should select the previously created Tile Map, and where to place the uasset file within the `Content` folder. It is recommended to place the imported file in the same folder as the Tiled file.

**Note:** You can set up some Unreal Engine properties on the tile map (such as `Pixels Per Unreal Unit` or `Separation Per Layer`) from Tiled and will get automatically set up when importing. Check out the [Custom Properties](./custom-properties.html) for more information.

## Move/Rename a Tile Map
You can move/rename your imported files from within Unreal by just drag and droping the files in the Content Browser.

If you want to move/rename the original Tiled file you can do that on your OS File System and then click on `Change` in the Plugin UI next to the `Source`.

**Note:** When changing the source file of a tile map, the name of the file must match the previous name it had before.

## Reimport a Tile Map
If at some point you make changes to the Tile Map in Tiled and you want to bring them over to Unreal Engine, is just as easy as clicking `Reimport` on the plugin UI. 

Alternatively, you can automate the process by enabling the `Auto Reimport` feature, which will reimport the asset when it detects any changes.

## Delete an imported Tile Map
To delete an imported Tile Map, click on the `Delete` button in the plugin UI and it will delete the Tile Map and any embedded Tile Sets that were imported with it.

**Note:** Do not try to delete the files imported to Unreal Engine manually, as it will cause issues with the plugin. Always use the plugin UI to manage the imported files.

**Note:** Embedded files (such as tile sets or flipbooks) can't be deleted manually and will only get removed when the owning file is deleted.