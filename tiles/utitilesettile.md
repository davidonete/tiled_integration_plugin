---
layout: default
---

[Home](../) / [Tiles](./index.md) / Classes / UTITileSetTile

# UTITileSetTile

## Description
This an individual Tile stored in a [Tile Set](./tilesets/utitileset.md) that was imported from Tiled and can only be modified from Tiled when importing or reimporting.

## Extend Class
If you want to extend the class either via C++ or Blueprint, you can specify in the [Plugin Settings](../settings/index.md) what class the plugin should use, instead of the default one. Keep in mind that your class must be a child class from the original one you want to extend.
 
**Note:** Setting a new class override to be used by the plugin won't be applied to previously imported assets, you will have to delete and import the already existing assets after the settings have been changed.

## Functions

### HasCollision

**C++** &#9989; **Blueprint** &#9989;

Checks if the Tile has collision set up.

**Return**
- **bool:** True if the Tile has collision.

### GetCustomProperties

**C++** &#9989; **Blueprint** &#9989;

Gets the [Custom Properties](../custom-properties/index.md) of the Tile, where you can access all the individual properties stored for the Tile.

**Return**
- **UTICustomProperties*:** The [Custom Properties](../custom-properties/index.md) of the Tile.

### GetUserData

**C++** &#9989; **Blueprint** &#9989;

Gets the User Data name of the Tile (can be specified in the [Custom Properties](./custom-properties.html).

**Return**
- **FName:** The User Data name of the tile.

### GetTileSet

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile Set](../tilesetes/utitileset.html) that contains this Tile.

**Return**
- **UTITileSet*:** [Tile Set](../tilesetes/utitileset.html) that contains this Tile.

### GetTileSetIndex

**C++** &#9989; **Blueprint** &#9989;

Gets the Tile Set Index used by this Tile.

**Return**
- **int32:** Tile Set Index used by this Tile.

### GetSize

**C++** &#9989; **Blueprint** &#9989;

Gets the Tile size (in pixels).

**Return**
- **FIntPoint:** The Tile size.

### IsValid

**C++** &#9989; **Blueprint** &#9989;

Checks if the Tile has a Tile Set and Tile Set Index assigned correctly.

**Return**
- **bool:** True if the Tile has a Tile Set and Tile Set Index assigned.

### IsAnimated

**C++** &#9989; **Blueprint** &#9989;

Checks if the Tile has animation set up.

**Return**
- **bool:** True if the Tile has animation.

### GetFlipbook

**C++** &#9989; **Blueprint** &#9989;

Gets the Tile animation flipbook.

**Return**
- **UPaperFlipbook*:** The animation flipbook or null if not set.

### GetOpacity

**C++** &#9989; **Blueprint** &#9989;

Gets the opacity of this Tile specified in the [Custom Properties](./custom-properties.html).

**Return**
- **float:** The opacity of this Tile.

### GetGroupID

**C++** &#9989; **Blueprint** &#9989;

Gets the Group ID specified in the [Custom Properties](./custom-properties.html).

**Return**
- **int32:** The Group ID.

### OnCustomPropertiesLoaded (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the [Custom Properties](../custom-properties/index.md) have been loaded.

**Arguments**
- **Properties:** [Custom Properties](../custom-properties/index.md) loaded.

### OnImported (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile has been imported by the plugin.