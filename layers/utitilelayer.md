---
layout: default
---

[Home](../) / [Tile Layers](./index.md) / Classes / UTITileLayer

# UTITileLayer

## Description
This is the Tile Layer in a [Tile Map](../tilemaps/utitilemap.html) asset that was imported from Tiled and can only be modified from Tiled when importing or reimporting.

## Extend Class
If you want to extend the class either via C++ or Blueprint, you can specify in the [Plugin Settings](../settings/index.md) what class the plugin should use, instead of the default one. Keep in mind that your class must be a child class from the original one you want to extend.
 
**Note:** Setting a new class override to be used by the plugin won't be applied to previously imported assets, you will have to delete and import the already existing assets after the settings have been changed.

## Functions
### ForEachTile

**C++** &#9989; **Blueprint** &#10060;

Calls the given callback once per tile coordinate within the Tile Layer. The [Tile Map Tile](../tiles/utitilemaptile.html) returned may be null.

**Arguments**
- **Callback:** The function/lambda to be called per tile coordinate.
- **Reversed:** Set to true to change the order from last to first. If false the order will be from first to last.

### ForEachOccupiedTile

**C++** &#9989; **Blueprint** &#10060;

Calls the given callback once per [Tile Map Tile](../tiles/utitilemaptile.html) stored in the Tile Layer.

**Arguments**
- **Callback:** The function/lambda to be called per [Tile Map Tile](../tiles/utitilemaptile.html).
- **Reversed:** Set to true to change the order from last to first. If false the order will be from first to last.

### GetNumOccupiedTiles

**C++** &#9989; **Blueprint** &#10060;

Gets the amount of Tiles in this Tile Layer.

**Return**
- **int32:** The amount of Tiles

### GetElevation

**C++** &#9989; **Blueprint** &#10060;

Gets the Tile Layer elevation (specified on the [Custom Properties](./custom-properties.html) or by the layer order)

**Return**
- **int32:** The elevation level

### GetElevationOffset

**C++** &#9989; **Blueprint** &#10060;

Gets the Tile Layer elevation offset (specified on the [Custom Properties](./custom-properties.html))

**Return**
- **float:** The elevation offset amount

### GetCustomProperties

**C++** &#9989; **Blueprint** &#9989;

Gets the [Custom Properties](../custom-properties/index.md) of the Tile Layer, where you can access all the individual properties stored for the Tile Layer.

**Return**
- **UTICustomProperties*:** The [Custom Properties](../custom-properties/index.md) of the Tile Layer.

### GetTile

**C++** &#9989; **Blueprint** &#9989;

Tries to get the [Tile Map Tile](../tiles/utitilemaptile.html) stored in the specified coordinates.

**Arguments**
- **X:** The horizontal coordinate within the Tile Layer.
- **Y:** The vertical coordinate within the Tile Layer.

**Return**
- **UTITileMapTile*:** The [Tile Map Tile](../tiles/utitilemaptile.html) if there is a Tile in that coordinate, or null if it doesn't contain any Tiles.

### GetTileMap

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile Map](../tilemaps/utitilemap.html) that contains this Tile Layer.

**Return**
- **UTITileMap*:** The [Tile Map](../tilemaps/utitilemap.html) that contains this layer.

### GetLayerIndex

**C++** &#9989; **Blueprint** &#9989;

Gets the Tile Layer index.

**Return**
- **int32:** The layer index.

### IsCollisionEnabled

**C++** &#9989; **Blueprint** &#9989;

Check if the collision is enabled for this Tile Layer (set up from the [Custom Properties](../custom-properties/index.md)).

**Return**
- **bool:** If the collision is enabled.

### IsHidden

**C++** &#9989; **Blueprint** &#9989;

Check if the Tile Layer is hidden.

**Return**
- **bool:** If the layer is hidden.

### GetCollisionThickness

**C++** &#9989; **Blueprint** &#9989;

Gets the Tile Layer collision thickness (set up from the [Custom Properties](../custom-properties/index.md)).

**Return**
- **float:** The collision thickness of this Tile Layer.

### GetCollisionThickness

**C++** &#9989; **Blueprint** &#9989;

Gets the Tile Layer collision offset (set up from the [Custom Properties](../custom-properties/index.md)).

**Return**
- **float:** The collision offset of this Tile Layer.

### TileCoordinatesToTileIndex

**C++** &#9989; **Blueprint** &#10060;

Converts the given tile coordinates to tile index.

**Arguments**
- **X:** The horizontal coordinate within the [Tile Layer](../layers/utitilelayer.html).
- **Y:** The vertical coordinate within the [Tile Layer](../layers/utitilelayer.html).

**Return**
- **int32:** The tile index of the given coordinates.

### TileIndexToTileCoordinates

**C++** &#9989; **Blueprint** &#10060;

Converts the given tile index to tile coordinates.

**Arguments**
- **TileIndex:** The tile index to convert.

**Return**
- **FIntVector:** The tile coordinates of the given tile index.

### OnCustomPropertiesLoaded (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile Map [Custom Properties](../custom-properties/index.md) have been loaded.

**Arguments**
- **Properties:** [Custom Properties](../custom-properties/index.md) loaded.

### OnImported (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile Layer has been imported by the plugin.