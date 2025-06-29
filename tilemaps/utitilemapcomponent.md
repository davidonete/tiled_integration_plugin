---
layout: default
---

[Home](../) / [Tile Maps](./index.md) / Classes / UTITileMapComponent

# UTITileMapComponent

## Description
This is the component that takes care of rendering the [Tile Map Instance](./utitilemapinstance.html) and is part of a [Tile Map Actor](./atitilemapactor.html).

## Extend Class
If you want to extend the class either via C++ or Blueprint, you can specify in the [Plugin Settings](../settings/index.md) what class the plugin should use, instead of the default one. Keep in mind that your class must be a child class from the original one you want to extend.
 
**Note:** Setting a new class override to be used by the plugin won't be applied to previously imported assets, you will have to delete and import the already existing assets after the settings have been changed.

## Functions
### GetTileMapInstance

**C++** &#9989; **Blueprint** &#10060;

Gets the [Tile Map Instance](./utitilemapinstance.html) used by the Tile Map Component.

**Return**
- **UTileMapInstance:** The [Tile Map Instance](./utitilemapinstance.html) used.

### GetTileMapActor

**C++** &#9989; **Blueprint** &#10060;

Gets the [Tile Map Actor](./atitilemapcomponent.html) that uses this Tile Map Component.

**Return**
- **ATileMapActor:** The [Tile Map Actor](./atitilemapcomponent.html).