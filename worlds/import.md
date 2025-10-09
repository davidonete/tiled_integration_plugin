---
layout: default
---

[Home](../) / [Tile Worlds](./index.md) / Import a Tile World

## Import a Tile World
On this guide we will go over the steps to importing a tile world from Tiled to Unreal Engine as well as some tips and tricks to make the process easier.

**1.-** The first step is to create a Tile World in Tiled and add one or more [Tile Maps](../tilemaps/index.md) into it.

**Note:** The Tile World file should be placed within the `Content` folder of your project in order to allow moving the project around and use the reimport feature. It is recommended to place your files in a folder structure like `<Project Folder>/Content/TileWorlds/<YourTileWorldFolder>/<YourTileWorld>.world`

**2.-** Finally, to import the Tile World to Unreal Engine, click the `Import` button on the plugin UI and follow the instructions. It will ask the file to import, where you should select the previously created Tile World, and where to place the uasset file within the `Content` folder. It is recommended to place the imported file in the same folder as the Tiled file.

**Note:** If the plugin detects a tile map used by the tile world that is not already imported, it will try to import it as a dependency of the added tile world.

## Move/Rename a Tile World
You can move/rename your imported files from within Unreal by just drag and droping the files in the Content Browser.

If you want to move/rename the original Tiled file you can do that on your OS File System and then click on `Change` in the Plugin UI next to the `Source`.

## Reimport a Tile World
If at some point you make changes to the Tile World in Tiled and you want to bring them over to Unreal Engine, is just as easy as clicking `Reimport` on the plugin UI. 

Alternatively, you can automate the process by enabling the `Auto Reimport` feature, which will reimport the asset when it detects any changes.

## Delete an imported Tile World
To delete an imported Tile World, click on the `Delete` button in the plugin UI and it will delete the Tile World.

**Note:** Do not try to delete the files imported to Unreal Engine manually, as it will cause issues with the plugin. Always use the plugin UI to manage the imported files.

**Note:** Embedded files (such as tile maps) can't be deleted manually and will only get removed when the owning file is deleted.