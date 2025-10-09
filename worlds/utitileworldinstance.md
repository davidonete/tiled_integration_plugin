---
layout: default
---

[Home](../) / [Tile Worlds](./index.md) / Classes / UTITileWorldInstance

# UTITileWorldInstance

## Description
his is an instance of a [UTITileWorld](./utitileworld.html) that will get created when you add the asset to a level and can be modified at runtime (for example, by adding/removing maps)

## Extend Class
If you want to extend the class either via C++ or Blueprint, you can specify in the [Plugin Settings](../settings/index.md) what class the plugin should use, instead of the default one. Keep in mind that your class must be a child class from the original one you want to extend.
 
**Note:** Setting a new class override to be used by the plugin won't be applied to previously imported assets, you will have to delete and import the already existing assets after the settings have been changed.

## Functions
### GetTileWorld

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile World](./utitileworld.html) asset used by this Tile World Instance.

**Return**
- **UTITileWorld:** The [Tile World](./utitileworld.html) asset used by this Tile World Instance.

### GetTileWorldActor

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile World Actor](./atitileworldactor.html) that owns this Tile World Instance.

**Return**
- **ATITileWorldActor*:** The [Tile World Actor](./atitileworldactor.html) that owns this Tile World Instance.

### UsesTileWorld

**C++** &#9989; **Blueprint** &#9989;

Checks if the Tile World Instance uses the given [Tile World](./utitileworld.html) asset.

**Arguments**
- **TileWorld:** The [Tile World](./utitileworld.html) asset to check. 

**Return**
- **bool:** True if the Tile World Instance uses the given [Tile World](./utitileworld.html) asset.

### GetTileMaps

**C++** &#9989; **Blueprint** &#9989;

Gets an array of [Tile Map Components](./utitilemapcomponent.html) that are instantiated for this Tile World Instance.

**Return**
- **TArray<FTITileWorldInstanceMapData>&:** An array of [Tile Map Components](./utitilemapcomponent.html) instanced for this Tile World Instance.

### UsesTileMap

**C++** &#9989; **Blueprint** &#9989;

Checks if the Tile World Instance uses the given [Tile Map](../tilemaps/utitilemap.html) asset.

**Arguments**
- **TileMap:** [Tile Map](../tilemaps/utitilemap.html) asset to check.

**Return**
- **bool:** True if the Tile World Instance uses the given [Tile Map](../tilemaps/utitilemap.html) asset.

### AddTileMap

**C++** &#9989; **Blueprint** &#9989;

Adds a new [Tile Map](../tilemaps/utitilemap.html) to the Tile World Instance.

**Arguments**
- **TileMapData:** A struct with a reference to the [Tile Map](../tilemaps/utitilemap.html) asset to use and the 2D coordinates to place it.
- **Classes:** The list of TileIntegration classes to use for creating this map.
- **bTemplate:** (internal use only)
- **bCreateComponent:** (internal use only)

**Return**
- **FTITileWorldInstanceMapData:** A reference to the newly added map

### RemoveTileMap

**C++** &#9989; **Blueprint** &#9989;

Removes a existing [Tile Map](../tilemaps/utitilemap.html) from the Tile World Instance.

**Arguments**
- **TileMap:** A reference to an existing [Tile Map](../tilemaps/utitilemap.html) (gathered from ```AddTileMap``` or ```GetTileMaps```)

### OnInstanced (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile World Instance has been added to a level.