---
layout: default
---

[Home](../) / [Tile Maps](./index.md) / Classes / UTITileMap

# UTITileMap

## Description
This class represents the actual tile map asset that has been imported from a Tiled Tile Map file and can only be modified from the Tiled Map Editor software and later imported/reimported to Unreal Engine.

## Extend Class
If you want to extend the class either via C++ or Blueprint, you can specify in the [Plugin Settings](../settings/index.md) what class the plugin should use, instead of the default one. Keep in mind that your class must be a child class from the original one you want to extend.
 
**Note:** Setting a new class override to be used by the plugin won't be applied to previously imported assets, you will have to delete and import the already existing assets after the settings have been changed.

**Blueprint:** &#9989;

**C++:** &#10060;

## Functions
### GetCustomProperties
Returns the [Custom Properties](../custom-properties/index.md) of the Tile Map, where you can access all the individual properties stored for the Tile Map.

**Blueprint:** &#9989;

**C++:** &#9989;

### GetTile
Returns the [Tile Map Tile](../tiles/utitilemaptile.md) stored in the specified coordinates, where `X` and `Y` are the coordinates within the [Tile Layer](../layers/utitilelayer.html) and `Z` is the layer index (from highest to lowest).

**Blueprint:** &#9989;

**C++:** &#9989;
