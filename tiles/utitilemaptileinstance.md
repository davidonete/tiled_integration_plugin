---
layout: default
---

[Home](../) / [Tiles](./index.md) / Classes / UTITileMapTileInstance

# UTITileMapTileInstance

## Description
This is an instance of a [UTITileMapTile](./utitilemaptile.html) stored in a [Tile Map Instance](../tilemaps/utitilemapinstance.html) that will get created when you add a [Tile Map](./tilemaps/utitilemap.html) to a level and can be modified at runtime (for example, by adding/removing tiles)

## Extend Class
If you want to extend the class either via C++ or Blueprint, you can specify in the [Plugin Settings](../settings/index.md) what class the plugin should use, instead of the default one. Keep in mind that your class must be a child class from the original one you want to extend.
 
**Note:** Setting a new class override to be used by the plugin won't be applied to previously imported assets, you will have to delete and import the already existing assets after the settings have been changed.

## Functions

### GetTileSetTile

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile Set Tile](./utitilesettile.html) used by this Tile Instance.

**Return**
- **UTITileSetTile*:** The [Tile Set Tile](./utitilesettile.html) used by this Tile Instance.

### GetCustomProperties

**C++** &#9989; **Blueprint** &#9989;

Gets the [Custom Properties](../custom-properties/index.md) of the Tile Instance, where you can access all the individual properties stored for the Tile Instance.

**Return**
- **UTICustomProperties*:** The [Custom Properties](../custom-properties/index.md) of the Tile Instance.

### HasCollision

**C++** &#9989; **Blueprint** &#9989;

Checks if the Tile Instance has collision set up on the [Tile Set Tile](./utitilesettile.html).

**Return**
- **bool:** True if the Tile Instance has collision.

### GetTileSet

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile Set](../tilesetes/utitileset.html) used by this Tile Instance.

**Return**
- **UTITileSet*:** [Tile Set](../tilesetes/utitileset.html) used by this Tile Instance.

### GetTileSetIndex

**C++** &#9989; **Blueprint** &#9989;

Gets the Tile Set Index used by this Tile Instance.

**Return**
- **int32*:** Tile Set Index used by this Tile Instance.

### GetGroupID

**C++** &#9989; **Blueprint** &#9989;

Gets the Group ID specified in the [Tile Set Tile](./utitilesettile.html).

**Return**
- **int32:** The Group ID.

### GetGroup

**C++** &#9989; **Blueprint** &#9989;

Gets the [Group of Tiles](./utitilemaptilegroup.html) specified in the [Tile Set Tile](./utitilesettile.html).

**Return**
- **UTITileMapTileGroup*:** [Group of Tiles](./utitilemaptilegroup.html) specified in the [Tile Set Tile](./utitilesettile.html).

### GetTileMapComponent

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile Map Component](../tilemaps/utitilemapcomponent.html) used by this Tile Instance.

**Return**
- **UTITileMapComponent*:** [Tile Map Component](../tilemaps/utitilemapcomponent.html) used by this Tile Instance.

### GetTileMapInstance

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile Map Instance](../tilemaps/utitilemapinstance.html) that contains this Tile Instance.

**Return**
- **UTITileMapActor:** [Tile Map Actor](./utitilemapactor.html) that contains this Tile Instance.

### GetLayerInstance

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile Layer Instance](../layers/utitilelayerinstance.html) that contains this Tile Instance.

**Return**
- **UTITileLayerInstance:** [Tile Layer Instance](../layers/utitilelayerinstance.html) that contains this Tile Instance.

### GetCoordinates

**C++** &#9989; **Blueprint** &#9989;

Gets the coordinates of this Tile Instance within the [Tile Map](../tilemaps/utitilemapinstance.html).

**Return**
- **FIntVector:** The coordinates of this Tile Instance.

### GetOpacity

**C++** &#9989; **Blueprint** &#9989;

Gets the opacity of this Tile Instance.

**Return**
- **float:** The opacity of this Tile Instance.

### SetOpacity

**C++** &#9989; **Blueprint** &#9989;

Gets the opacity of this Tile Instance.

**Arguments**
- **InOpacity:** The new opacity for this Tile Instance.

### IsAnimated

**C++** &#9989; **Blueprint** &#9989;

Checks if the Tile Instance has animation set up on the [Tile Set Tile](./utitilesettile.html).

**Return**
- **bool:** True if the Tile Instance has animation.

### GetFlipbook

**C++** &#9989; **Blueprint** &#9989;

Gets the Tile Instance animation flipbook.

**Return**
- **UPaperFlipbook*:** The animation flipbook or null if not set.

### IsInViewport

**C++** &#9989; **Blueprint** &#9989;

Checks if the Tile Instance is currently visible in the viewport.

**Return**
- **bool:** True if the Tile Instance is visible in the viewport.

### GetTilePosition

**C++** &#9989; **Blueprint** &#9989;

Gets the top left corner position of this Tile Instance.

**Arguments**
- **bWorldSpace:** If the returned position should be in world space of local space (within the Tile Map)

**Return**
- **FVector:** The top left corner position of the Tile Instance.

### GetElevation

**C++** &#9989; **Blueprint** &#9989;

Gets the elevation of the owning [Tile Layer](../layers/utitilelayerinstance.html)

**Return**
- **int32:** The elevation of the owning [Tile Layer](../layers/utitilelayerinstance.html)

### DebugDraw (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Draws debug lines around the Tile Instance.

**Arguments**
- **Duration:** How long the debug draw should last (in seconds)
- **Color:** The color of the debug draw lines.

### OnInstanced (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile Instance has been added to a level.

### OnModified (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile Instance has been modified.

**Arguments**
- **Event:** The type of modification (TileAdded, TileRemoved, TileModified).
- **AffectedObject:** The object that has been modified (The class will vary depending on the type of event).

### OnPostLoad (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile Instance has been loaded.

### OnTick (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile Instance ticks.

**Arguments**
- **DeltaTime:** Time (in seconds) since last tick.

### ShouldGroupWithTile (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when making the [Tile Groups](./utitilemaptilegroup.html)

**Arguments**
- **GroupTile:** Another Tile Instance that wants to group with this Tile Instance.

**Return**
- **bool:** Return true if this Tile Instance should be grouped with the GroupTile.