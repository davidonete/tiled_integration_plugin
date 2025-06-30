---
layout: default
---

[Home](../) / [Tile Sets](./index.md) / Import a Tile Set

## Import a Tile Set
On this guide we will go over the steps to importing a tile set from Tiled to Unreal Engine as well as some tips and tricks to make the process easier.

[Quick Video Guide](https://www.youtube.com/watch?v=AQnpu9husAo)

**1.-** The first step is to create a Tile Set in Tiled (you can skip this step if you want to embed the Tile Set into the [Tile Map](../tilemaps/index.md)).

**Note:** The plugin supports both embedded Tile Sets (which lives inside the [Tile Map](../tilemaps/index.md) and will be imported with it) or standalone Tile Sets (in a sepparate file). It is recommended to use standalone Tile Sets, so you can reuse them in different tile maps.

**Note:** At this time, the plugin only supports the **tsj** and **json** file extensions.

**Note:** The Tile Set file should be placed within the `Content` folder of your project in order to allow moving the project around and use the reimport feature. It is recommended to place your files in a folder structure like `<Project Folder>/Content/TileSets/<YourTileSetFolder>/<YourTileSet>.json`

**2.-** Finally, to import the Tile Set to Unreal Engine, click the `Import` button on the plugin UI and follow the instructions. It will ask the file to import, where you should select the previously created Tile Set, and where to place the uasset file within the `Content` folder. It is recommended to place the imported file in the same folder as the Tiled file.

**Note:** Moving/Renaming the imported files or the original Tiled files after being imported is currently not supported. If you need to move or rename a file, you will have to delete the imported asset using the plugin UI button and import it again. 

**Note:** You can set up some Unreal Engine properties on the tile set (such as `ConditionTexture`) from Tiled and will get automatically set up when importing. Check out the [Custom Properties](./custom-properties.html) for more information.

## Reimport a Tile Set
If at some point you make changes to the Tile Set in Tiled and you want to bring them over to Unreal Engine, is just as easy as clicking `Reimport` on the plugin UI. 

Alternatively, you can automate the process by enabling the `Auto Reimport` feature, which will reimport the asset when it detects any changes.

## Delete an imported Tile Set
To delete an imported Tile Set, click on the `Delete` button in the plugin UI and it will delete the Tile Set.

**Note:** Do not try to delete the files imported to Unreal Engine manually, as it will cause issues with the plugin. Always use the plugin UI to manage the imported files.