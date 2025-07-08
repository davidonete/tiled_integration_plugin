---
layout: default
---

[Home](../) / [Tile Layers](./index.md) / Classes / UTITileLayerInstance

# UTITileLayerInstance

## Description
This is an instance of a [UTITileLayer](./utitilelayer.html) that will get created when you add the asset to a level and can be modified at runtime (for example, by adding/removing tiles)

## Extend Class
If you want to extend the class either via C++ or Blueprint, you can specify in the [Plugin Settings](../settings/index.md) what class the plugin should use, instead of the default one. Keep in mind that your class must be a child class from the original one you want to extend.
 
**Note:** Setting a new class override to be used by the plugin won't be applied to previously imported assets, you will have to delete and import the already existing assets after the settings have been changed.

## Functions
### GetTile

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile Layer](../layers/utitilelayer.html) asset for the layer instance.

**Return**
- **UTITileLayer*:** The [Tile Layer](../layers/utitilelayer.html) used to initialize this layer instance.

### GetCustomProperties

**C++** &#9989; **Blueprint** &#9989;

Gets the [Custom Properties](../custom-properties/index.md) of the Tile Layer, where you can access all the individual properties stored for the Tile Layer.

**Return**
- **UTICustomProperties*:** The [Custom Properties](../custom-properties/index.md) of the Tile Layer.

### GetTileInstance

**C++** &#9989; **Blueprint** &#9989;

Tries to get the [Tile Map Tile Instance](../tiles/utitilemaptileinstance.html) stored in the specified coordinates.

**Arguments**
- **X:** The horizontal coordinate within the Tile Layer.
- **Y:** The vertical coordinate within the Tile Layer.

**Return**
- **UTITileMapTileInstance*:** The [Tile Map Tile Instance](../tiles/utitilemaptileinstance.html) if there is a Tile in that coordinate, or null if it doesn't contain any Tiles.

### SetTileInstance

**C++** &#9989; **Blueprint** &#9989;

Sets a [Tile Map Tile Instance](../tiles/utitilemaptileinstance.html) in the given coordinates.

**Arguments**
- **X:** The horizontal coordinate within the [Tile Layer Instance](../layers/utitilelayerinstance.html).
- **Y:** The vertical coordinate within the [Tile Layer Instance](../layers/utitilelayerinstance.html).
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

### GetTileMapComponent

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile Map Component](../tilemaps/utitilemapcomponent.html) used by this Tile Layer Instance.

**Return**
- **UTITileMapComponent*:** [Tile Map Component](../tilemaps/utitilemapcomponent.html) used by this Tile Layer Instance.

### GetTileMapActor

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile Map Actor](../tilemaps/utitilemapactor.html) used by this Tile Layer Instance.

**Return**
- **UTITileMapActor*:** [Tile Map Actor](../tilemaps/utitilemapactor.html) used by this Tile Layer Instance.

### GetTileMapInstance

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile Map Instance](../tilemaps/utitilemapinstance.html) that contains this Tile Layer Instance.

**Return**
- **UTITileMapActor:** [Tile Map Actor](./utitilemapactor.html) that contains this Tile Layer Instance.

### GetLayerName

**C++** &#9989; **Blueprint** &#9989;

Gets the name of this Tile Layer.

**Return**
- **FString:** The name of the Tile Layer.

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

### OnInstanced (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile Layer Instance has been added to a level.

### OnModified (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile Layer Instance has been modified.

**Arguments**
- **Event:** The type of modification (TileAdded, TileRemoved, TileModified).
- **AffectedObject:** The object that has been modified (The class will vary depending on the type of event).

### OnPostLoad (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile Layer Instance has been loaded.

### OnTick (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile Layer Instance ticks.

**Arguments**
- **DeltaTime:** Time (in seconds) since last tick.