---
layout: default
---

[Home](../) / [Tile Worlds](./index.md) / Classes / ATITileWorldActor

# ATITileWorldActor

## Description
This is the actor that will be created when instancing a [Tile World](./utitileworld.html) asset, which contains a group of [Tile Map Components](../tilemaps/utitilemapcomponent.html) that takes care of rendering every [Tile Map Instances](./utitilemapinstance.html).

## Extend Class
If you want to extend the class either via C++ or Blueprint, you can specify in the [Plugin Settings](../settings/index.md) what class the plugin should use, instead of the default one. Keep in mind that your class must be a child class from the original one you want to extend.
 
**Note:** Setting a new class override to be used by the plugin won't be applied to previously imported assets, you will have to delete and import the already existing assets after the settings have been changed.

## Functions
### GetTileWorld

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile World](./utitileworld.html) asset used by this Tile World Actor.

**Return**
- **UTITileWorld:** The [Tile World](./utitileworld.html) asset used by this Tile World Actor.

### GetTileWorldInstance

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile World Instance](./utitileworldinstance.html) used by this Tile World Actor.

**Return**
- **UTITileWorld:** The [Tile World Instance](./utitileworldinstance.html) asset used by this Tile World Actor.

### UsesTileWorld

**C++** &#9989; **Blueprint** &#9989;

Checks if the Tile World Instance uses the given [Tile World](./utitileworld.html) asset.

**Arguments**
- **TileWorld:** The [Tile World](./utitileworld.html) asset to check. 

**Return**
- **bool:** True if the Tile World Instance uses the given [Tile World](./utitileworld.html) asset.

### UsesTileMap

**C++** &#9989; **Blueprint** &#9989;

Checks if the Tile World Instance uses the given [Tile Map](../tilemaps/utitilemap.html) asset.

**Arguments**
- **TileMap:** [Tile Map](../tilemaps/utitilemap.html) asset to check.

**Return**
- **bool:** True if the Tile World Instance uses the given [Tile Map](../tilemaps/utitilemap.html) asset.

### GetClasses

**C++** &#9989; **Blueprint** &#9989;

Gets the classes used to create the Tile World Actor and other dependencies.

**Return**
- **FTITileClasses:** The classes used to create the Tile World Actor and other dependencies.

### OnInstanced (Overrideable)

**C++** &#9989; **Blueprint** &#9989;

Called when the Tile World Instance has been added to a level.

### SpawnTileWorld

**C++** &#9989; **Blueprint** &#9989;

Spawns a Tile World Actor with the given parameters

**Arguments**
- **WorldContextObject:** The world context where the Tile Map Actor will spawn to.
- **TileWorld:** The [Tile World](./utitileworld.html) to spawn.
- **Position:** The position of the spawned Tile Map Actor.
- **Rotation:** The rotation of the spawned Tile Map Actor.
- **Classes:** The classes to use for creating the Tile World Actor and other dependencies.

**Return**
- **ATITileWorldActor:** The Tile World Actor spawned.