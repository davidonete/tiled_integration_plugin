---
layout: default
---

[Home](../) / [Tile Maps](./index.md) / Classes / UTITileMapInstance

# UTITileMapInstance

## Description
This is an instance of a [UTITileMap](./utitilemap.html) that will get created when you add the asset to a level and can be modified at runtime (for example, by adding/removing tiles)

## Extend Class
If you want to extend the class either via C++ or Blueprint, you can specify in the [Plugin Settings](../settings/index.md) what class the plugin should use, instead of the default one. Keep in mind that your class must be a child class from the original one you want to extend.
 
**Note:** Setting a new class override to be used by the plugin won't be applied to previously imported assets, you will have to delete and import the already existing assets after the settings have been changed.

## Functions
### GetTileMap

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile Map](./utitilemap.html) used by this Tile Map Instance.

**Return**
- **UTITileMap*:** The [Tile Map](./utitilemap.html) used by this Tile Map Instance.

## Functions
### GetCustomProperties

**C++** &#9989; **Blueprint** &#9989;

Gets the [Custom Properties](../custom-properties/index.md) of the Tile Map, where you can access all the individual properties stored for the Tile Map.

**Return**
- **UTICustomProperties*:** The [Custom Properties](../custom-properties/index.md) of the Tile Map.

### GetLayerInstance

**C++** &#9989; **Blueprint** &#9989;

Tries to get the [Tile Layer Instance](../layers/utitilelayerinstance.html) in the Tile Map Instance.

**Arguments**
- **LayerIndex:** The layer index (from highest to lowest).

**Return**
- **UTITileLayerInstance*:** The [Tile Layer Instance](../layers/utitilelayerinstance.html) or null if not found.

### GetTileInstance

**C++** &#9989; **Blueprint** &#9989;

Tries to get the [Tile Map Tile Instance](../tiles/utitilemaptileinstance.html) stored in the specified coordinates.

**Arguments**
- **X:** The horizontal coordinate within the [Tile Layer Instance](../layers/utitilelayerinstance.html).
- **Y:** The vertical coordinate within the [Tile Layer Instance](../layers/utitilelayerinstance.html).
- **Z:** The [Tile Layer Instance](../layers/utitilelayerinstance.html) index (from highest to lowest).

**Return**
- **UTITileMapTileInstance*:** The [Tile Map Tile Instance](../tiles/utitilemaptileinstance.html) if there is a Tile in that coordinate, or null if it doesn't contain any Tiles.

### SetTileInstance

**C++** &#9989; **Blueprint** &#9989;

Sets a [Tile Map Tile Instance](../tiles/utitilemaptileinstance.html) in the given coordinates.

**Arguments**
- **X:** The horizontal coordinate within the [Tile Layer Instance](../layers/utitilelayerinstance.html).
- **Y:** The vertical coordinate within the [Tile Layer Instance](../layers/utitilelayerinstance.html).
- **Z:** The [Tile Layer Instance](../layers/utitilelayerinstance.html) index (from highest to lowest).
- **TileSet:** The [Tile Set](../tilesets/utitileset.html) that will be used for this tile.
- **TileSetIndex:** The Tile Set Tile index that will be set for this tile.

**Return**
- **UTITileMapTileInstance*:** The [Tile Map Tile Instance](../tiles/utitilemaptileinstance.html) modified, or null if failed to set.

### UnsetTileInstance

**C++** &#9989; **Blueprint** &#9989;

Removes a [Tile Map Tile Instance](../tiles/utitilemaptileinstance.html) from the given coordinates.

**Arguments**
- **X:** The horizontal coordinate within the [Tile Layer Instance](../layers/utitilelayerinstance.html).
- **Y:** The vertical coordinate within the [Tile Layer Instance](../layers/utitilelayerinstance.html).
- **Z:** The [Tile Layer Instance](../layers/utitilelayerinstance.html) index (from highest to lowest).

### FindLayerInstancesByName

**C++** &#9989; **Blueprint** &#9989;

Retrieves a list of [Tile Layer Instances](../layers/utitilelayerinstance.html) whose names match the one specified. The search is case sensitive.

**Arguments**
- **LayerName:** The name of the [Tile Layer Instance](../layers/utitilelayerinstance.html) to look for (Case sensitive).

**Return**
- **TArray<UTITileLayerInstance*>:** A list of [Tile Layer Instances](../layers/utitilelayerinstance.html) found.

### GetLayersAmount

**C++** &#9989; **Blueprint** &#9989;

Gets the amount of [Tile Layer Instances](../layers/utitilelayerinstances.html) in this Tile Map Instance.

**Return**
- **int32:** The amount ot [Tile Layer Instances](../layers/utitilelayerinstance.html)

### GetTileMapComponent

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile Map Component](./utitilemapcomponent.html) used by this Tile Map Instance.

**Return**
- **UTITileMapComponent*:** [Tile Map Component](./utitilemapcomponent.html) used by this Tile Map Instance.

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

### IsInViewport

**C++** &#9989; **Blueprint** &#9989;

Checks if the Tile Map Instance is currently visible in the viewport.

**Return**
- **bool:** True if the Tile Map Instance is visible in the viewport.

### GetGroups

**C++** &#9989; **Blueprint** &#9989;

Get all the [Tile Groups](../tiles/utitilemaptilegroup.html) of the Tile Map by the specified [Tile Set](../tilesets/utitileset.html) and Group ID.

**Arguments**
- **TileSet:** The [Tile Set](../tilesets/utitileset.html) of the group.
- **GroupID:** The ID of the group (specified in the [Tile Set Tile Custom Properties](../tiles/utitilesettile.html))

**Return**
- **TArray<UTITileMapTileGroup*>:** A list of groups found for the specified [Tile Set](../tilesets/utitileset.html) and Group ID.

### ForEachLayerInstance

**C++** &#9989; **Blueprint** &#9989;

Calls the given callback once per [Tile Layer Instance](../layers/utitilelayerinstance.html)

**Arguments**
- **Callback:** The function/lambda to be called per [Tile Layer Instance](../layers/utitilelayerinstance.html).
- **Reversed:** Set to true to change the order from last to first (lowest to highest). If false the order will be from first to last (highest to lowest).

### ForEachOccupiedTileInstance

**C++** &#9989; **Blueprint** &#10060;

Calls the given callback once per [Tile Map Tile Instance](../tiles/utitilemaptileinstance.html) stored in the Tile Map.

**Arguments**
- **Callback:** The function/lambda to be called per [Tile Map Tile Instance](../tiles/utitilemaptileinstance.html).
- **Reversed:** Set to true to change the order from last to first. If false the order will be from first to last.

### ForEachTileInstance

**C++** &#9989; **Blueprint** &#10060;

Calls the given callback once per tile coordinate within the Tile Map. The [Tile Map Tile Instance](../tiles/utitilemaptileinstance.html) returned may be null.

**Arguments**
- **Callback:** The function/lambda to be called per tile coordinate.
- **Reversed:** Set to true to change the order from last to first. If false the order will be from first to last.

### GetTilePositionInLocalSpace

**C++** &#9989; **Blueprint** &#10060;

Gets the local position of the given tile coordinates relative to the Tile Map.

**Arguments**
- **X:** The horizontal coordinate within the [Tile Layer Instance](../layers/utitilelayerinstance.html).
- **Y:** The vertical coordinate within the [Tile Layer Instance](../layers/utitilelayerinstance.html).
- **Z:** The [Tile Layer Instance](../layers/utitilelayerinstance.html) index (from highest to lowest).

**Return**
- **FVector:** The position of the given tile coordinates in local space.

### GetTileSeparation (Overrideable)

**C++** &#9989; **Blueprint** &#10060;

Gets how high the given tile is, used for sorting the tile rendering.

**Arguments**
- **X:** The horizontal coordinate within the [Tile Layer Instance](../layers/utitilelayerinstance.html).
- **Y:** The vertical coordinate within the [Tile Layer Instance](../layers/utitilelayerinstance.html).
- **Z:** The [Tile Layer Instance](../layers/utitilelayerinstance.html) index (from highest to lowest).

**Return**
- **float:** The height of the given tile.

### TileCoordinatesToTileIndex

**C++** &#9989; **Blueprint** &#10060;

Converts the given tile coordinates to tile index.

**Arguments**
- **X:** The horizontal coordinate within the [Tile Layer Instance](../layers/utitilelayerinstance.html).
- **Y:** The vertical coordinate within the [Tile Layer Instance](../layers/utitilelayerinstance.html).
- **Z:** The [Tile Layer Instance](../layers/utitilelayerinstance.html) index (from highest to lowest).

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

### OnInstanced (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile Map Instance has been added to a level.

### OnModified (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile Map Instance has been modified.

**Arguments**
- **Event:** The type of modification (TileAdded, TileRemoved, TileModified).
- **AffectedObject:** The object that has been modified (The class will vary depending on the type of event).

### OnPostLoad (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile Map Instance has been loaded.

### OnTick (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile Map Instance ticks.

**Arguments**
- **DeltaTime:** Time (in seconds) since last tick.