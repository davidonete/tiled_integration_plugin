---
layout: default
---

[Home](../) / [Tile Maps](./index.md) / Classes / ATileMapActor

# ATileMapActor

## Description
This is the actor that will be created when instancing a [Tile Map](./utitilemap.html) asset, which contains a [Tile Map Component](./utitilemapcomponent.html) that takes care of rendering the [Tile Map Instance](./utitilemapinstance.html).

## Extend Class
If you want to extend the class either via C++ or Blueprint, you can specify in the [Plugin Settings](../settings/index.md) what class the plugin should use, instead of the default one. Keep in mind that your class must be a child class from the original one you want to extend.
 
**Note:** Setting a new class override to be used by the plugin won't be applied to previously imported assets, you will have to delete and import the already existing assets after the settings have been changed.

## Functions
### GetTileMapInstance

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile Map Instance](./utitilemapinstance.html) used by the Tile Map Actor.

**Return**
- **UTileMapInstance:** The [Tile Map Instance](./utitilemapinstance.html) used.

### GetTileMapComponent

**C++** &#9989; **Blueprint** &#9989;

Gets the [Tile Map Component](./utitilemapcomponent.html) used by the Tile Map Actor.

**Return**
- **UTileMapComponent:** The [Tile Map Component](./utitilemapcomponent.html) used.