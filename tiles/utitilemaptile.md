---
layout: default
---

[Home](../) / [Tiles](./index.md) / Classes / UTITileMapTile

# UTITileMapTile

## Description
This is a individual Tile stored in a [Tile Map](../tilemaps/utitilemap.html) asset that was imported from Tiled and can only be modified from Tiled when importing or reimporting.

## Extend Class
If you want to extend the class either via C++ or Blueprint, you can specify in the [Plugin Settings](../settings/index.md) what class the plugin should use, instead of the default one. Keep in mind that your class must be a child class from the original one you want to extend.
 
**Note:** Setting a new class override to be used by the plugin won't be applied to previously imported assets, you will have to delete and import the already existing assets after the settings have been changed.

## Functions

### GetCustomProperties

**C++** &#9989; **Blueprint** &#9989;

Gets the [Custom Properties](../custom-properties/index.md) of the Tile, where you can access all the individual properties stored for the Tile.

**Return**
- **UTICustomProperties*:** The [Custom Properties](../custom-properties/index.md) of the Tile.

### GetTileSet

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile Set](../tilesetes/utitileset.html) used by this Tile.

**Return**
- **UTITileSet*:** [Tile Set](../tilesetes/utitileset.html) used by this Tile.

### GetTileSetIndex

**C++** &#9989; **Blueprint** &#9989;

Gets the Tile Set Index used by this Tile.

**Return**
- **int32*:** Tile Set Index used by this Tile.

### GetGroupID

**C++** &#9989; **Blueprint** &#9989;

Gets the Group ID specified in the [Tile Set Tile](./utitilesettile.html).

**Return**
- **int32:** Group ID specified in the [Tile Set Tile](./utitilesettile.html).

### GetTileSetTile

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile Set Tile](./utitilesettile.html) used by this Tile.

**Return**
- **UTITileSetTile*:** The [Tile Set Tile](./utitilesettile.html) used by this Tile.

### GetLayer

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile Layer](../layers/utitilelayer.html) that contains this Tile.

**Return**
- **UTITileLayer*:** The [Tile Layer](../layers/utitilelayer.html) that contains this Tile.

### GetTileMap

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile Map](../tilemaps/utitilemap.html) that contains this Tile.

**Return**
- **UTITileMap*:** The [Tile Map](../tilemaps/utitilemap.html) that contains this Tile.

### GetCoordinates

**C++** &#9989; **Blueprint** &#9989;

Gets the coordinates of this Tile within the [Tile Map](../tilemaps/utitilemap.html).

**Return**
- **FIntVector:** The coordinates of this Tile.

### GetElevation

**C++** &#9989; **Blueprint** &#9989;

Gets the elevation of the owning [Tile Layer](../layers/utitilelayer.html)

**Return**
- **int32:** The elevation of the owning [Tile Layer](../layers/utitilelayer.html)

### OnCustomPropertiesLoaded (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the [Custom Properties](../custom-properties/index.md) have been loaded.

**Arguments**
- **Properties:** [Custom Properties](../custom-properties/index.md) loaded.

### OnImported (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile has been imported by the plugin.