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

## Functions
### GetCustomProperties

**C++** &#9989; **Blueprint** &#9989;

Gets the [Custom Properties](../custom-properties/index.md) of the Tile Map, where you can access all the individual properties stored for the Tile Map.

**Return**
- **UTICustomProperties*:** The [Custom Properties](../custom-properties/index.md) of the Tile Map.

### GetTile

**C++** &#9989; **Blueprint** &#9989;

Tries to get the [Tile Map Tile](../tiles/utitilemaptile.html) stored in the specified coordinates.

**Arguments**
- **X:** The horizontal coordinate within the [Tile Layer](../layers/utitilelayer.html).
- **Y:** The vertical coordinate within the [Tile Layer](../layers/utitilelayer.html).
- **Z:** The [Tile Layer](../layers/utitilelayer.html) index (from highest to lowest).

**Return**
- **UTITileMapTile*:** The [Tile Map Tile](../tiles/utitilemaptile.html) if there is a Tile in that coordinate, or null if it doesn't contain any Tiles.

### GetLayer

**C++** &#9989; **Blueprint** &#9989;

Tries to get the [Tile Layer](../layers/utitilelayer.html) in the Tile Map.

**Arguments**
- **LayerIndex:** The layer index (from highest to lowest).

**Return**
- **UTITileLayer*:** The [Tile Layer](../layers/utitilelayer.html) or null if not found.

### FindLayersByName

**C++** &#9989; **Blueprint** &#9989;

Retrieves a list of [Tile Layers](../layers/utitilelayer.html) whose names match the one specified. The search is case sensitive.

**Arguments**
- **LayerName:** The name of the [Tile Layer](../layers/utitilelayer.html) to look for (Case sensitive).

**Return**
- **TArray<UTITileLayer*>:** A list of [Tile Layers](../layers/utitilelayer.html) found.

### GetLayersAmount

**C++** &#9989; **Blueprint** &#9989;

Gets the amount of [Tile Layers](../layers/utitilelayer.html) in this Tile Map.

**Return**
- **int32:** The amount of [Tile Layers](../layers/utitilelayer.html)

### GetTileWidth

**C++** &#9989; **Blueprint** &#9989;

Gets the width (in pixels) of an individual [Tile](../tiles/index.md). (All tiles in the Tile Map have the same width)

**Return**
- **int32:** The width of an individual [Tile](../tiles/index.md).

### GetTileHeight

**C++** &#9989; **Blueprint** &#9989;

Gets the height in pixels of an individual [Tile](../tiles/index.md). (All tiles in the Tile Map have the same height)

**Return**
- **int32:** The height of an individual [Tile](../tiles/index.md).

### GetMapWidth

**C++** &#9989; **Blueprint** &#9989;

Gets the amount of [Tiles](../tiles/index.md) that can fit horizontally in the Tile Map.

**Return**
- **int32:** The amount of [Tiles](../tiles/index.md) that can fit horizontally.

### GetMapHeight

**C++** &#9989; **Blueprint** &#9989;

Gets the amount of [Tiles](../tiles/index.md) that can fit vertically in the Tile Map.

**Return**
- **int32:** The amount of [Tiles](../tiles/index.md) that can fit vertically.

### GetProjectionMode

**C++** &#9989; **Blueprint** &#9989;

Gets the projection mode of the Tile Map.

**Return**
- **ETileMapProjectionMode::Type:** The projection mode of the Tile Map (Orthogonal, IsometricDiamond, IsometricStaggered or HexagonalStaggered).

### ForEachLayer

**C++** &#9989; **Blueprint** &#9989;

Calls the given callback once per [Tile Layer](../layers/utitilelayer.html)

**Arguments**
- **Callback:** The function/lambda to be called per [Tile Layer](../layers/utitilelayer.html).
- **Reversed:** Set to true to change the order from last to first (lowest to highest). If false the order will be from first to last (highest to lowest).

### ForEachOccupiedTile

**C++** &#9989; **Blueprint** &#10060;

Calls the given callback once per [Tile Map Tile](../tiles/utitilemaptile.html) stored in the Tile Map.

**Arguments**
- **Callback:** The function/lambda to be called per [Tile Map Tile](../tiles/utitilemaptile.html).
- **Reversed:** Set to true to change the order from last to first. If false the order will be from first to last.

### ForEachTile

**C++** &#9989; **Blueprint** &#10060;

Calls the given callback once per tile coordinate within the Tile Map. The [Tile Map Tile](../tiles/utitilemaptile.html) returned may be null.

**Arguments**
- **Callback:** The function/lambda to be called per tile coordinate.
- **Reversed:** Set to true to change the order from last to first. If false the order will be from first to last.

### GetTilePositionInLocalSpace

**C++** &#9989; **Blueprint** &#10060;

Gets the local position of the given tile coordinates relative to the Tile Map.

**Arguments**
- **X:** The horizontal coordinate within the [Tile Layer](../layers/utitilelayer.html).
- **Y:** The vertical coordinate within the [Tile Layer](../layers/utitilelayer.html).
- **Z:** The [Tile Layer](../layers/utitilelayer.html) index (from highest to lowest).

**Return**
- **FVector:** The position of the given tile coordinates in local space.

### GetTileSeparation (Overrideable)

**C++** &#9989; **Blueprint** &#10060;

Gets how high the given tile is, used for sorting the tile rendering.

**Arguments**
- **X:** The horizontal coordinate within the [Tile Layer](../layers/utitilelayer.html).
- **Y:** The vertical coordinate within the [Tile Layer](../layers/utitilelayer.html).
- **Z:** The [Tile Layer](../layers/utitilelayer.html) index (from highest to lowest).

**Return**
- **float:** The height of the given tile.

### TileCoordinatesToTileIndex

**C++** &#9989; **Blueprint** &#10060;

Converts the given tile coordinates to tile index.

**Arguments**
- **X:** The horizontal coordinate within the [Tile Layer](../layers/utitilelayer.html).
- **Y:** The vertical coordinate within the [Tile Layer](../layers/utitilelayer.html).
- **Z:** The [Tile Layer](../layers/utitilelayer.html) index (from highest to lowest).

**Return**
- **int32:** The tile index of the given coordinates.

### TileIndexToTileCoordinates

**C++** &#9989; **Blueprint** &#10060;

Converts the given tile index to tile coordinates.

**Arguments**
- **TileIndex:** The tile index to convert.
- **Layer:** The layer for the given tile index.

**Return**
- **FIntVector:** The tile coordinates of the given tile index.

### OnCustomPropertiesLoaded (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile Map [Custom Properties](../custom-properties/index.md) have been loaded.

**Arguments**
- **Properties:** [Custom Properties](../custom-properties/index.md) loaded.

### OnImported (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile Map has been imported by the plugin.