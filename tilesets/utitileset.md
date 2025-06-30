---
layout: default
---

[Home](../) / [Tile Sets](./index.md) / Classes / UTITileSet

# UTITileSet

## Description
This is the Tile Set asset that was imported from Tiled which contain a list of [Tile Set Tiles](../tiles/utitilesettile.html) and can only be modified from Tiled when importing or reimporting. 

## Extend Class
If you want to extend the class either via C++ or Blueprint, you can specify in the [Plugin Settings](../settings/index.md) what class the plugin should use, instead of the default one. Keep in mind that your class must be a child class from the original one you want to extend.
 
**Note:** Setting a new class override to be used by the plugin won't be applied to previously imported assets, you will have to delete and import the already existing assets after the settings have been changed.

## Functions
### ForEachTile

**C++** &#9989; **Blueprint** &#10060;

Calls the given callback once per tile index within the Tile Set. The [Tile Set Tile](../tiles/utitilesettile.html) returned may be null.

**Arguments**
- **Callback:** The function/lambda to be called per tile index.
- **Reversed:** Set to true to change the order from last to first. If false the order will be from first to last.

### GetTile

**C++** &#9989; **Blueprint** &#9989;

Tries to get the [Tile Set Tile](../tiles/utitilesettile.html) stored in the specified index.

**Arguments**
- **TileIndex:** The tile index within the Tile Set.

**Return**
- **UTITileSetTile*:** The [Tile Set Tile](../tiles/utitilesettile.html) if there is a Tile in that tile index, or null if it doesn't contain any Tiles.

### GetCustomProperties

**C++** &#9989; **Blueprint** &#9989;

Gets the [Custom Properties](../custom-properties/index.md) of the Tile Set, where you can access all the individual properties stored for the Tile Set.

**Return**
- **UTICustomProperties*:** The [Custom Properties](../custom-properties/index.md) of the Tile Set.

### OnCustomPropertiesLoaded (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile Map [Custom Properties](../custom-properties/index.md) have been loaded.

**Arguments**
- **Properties:** [Custom Properties](../custom-properties/index.md) loaded.

### OnImported (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile Map has been imported by the plugin.