---
layout: default
---

[Home](../) / [Tile Worlds](./index.md) / Classes / UTITileWorld

# UTITileWorld

## Description
 This is the Tile World asset that was imported from Tiled which contains a group of [Tile Maps](../worlds/utitileworld.html) and can only be modified from Tiled when importing or reimporting. 

## Extend Class
If you want to extend the class either via C++ or Blueprint, you can specify in the [Plugin Settings](../settings/index.md) what class the plugin should use, instead of the default one. Keep in mind that your class must be a child class from the original one you want to extend.
 
**Note:** Setting a new class override to be used by the plugin won't be applied to previously imported assets, you will have to delete and import the already existing assets after the settings have been changed.

## Functions
### GetTileMaps

**C++** &#9989; **Blueprint** &#9989;

Gets an array of [Tile Maps](./utitilemap.html) that are included in the Tile World.

**Return**
- **TArray<FTITileWorldMapData>&:** An array of [Tile Maps](./utitilemap.html) included in the Tile World.

### OnImported (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile World has been imported by the plugin.