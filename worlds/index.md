---
layout: default
---

[Home](../) / Tile Worlds

# Tile Worlds

## Table of Contents
- **[Import a Tile World](./import.html)**
- **[Create a Blueprint](./blueprint.html)**
- **Classes**
  - **[ATITileWorldActor](./atitileworldactor.html)**
  - **[UTITileWorld](./utitileworld.html)**
  - **[UTITileWorldInstance](../tiles/utitileworldinstance.html)**
  
## Description
A Tile World is a collection of individual [Tile Maps](../tilemaps/utitilemap.html) each one having specific 2D coordinates. To create and modify a tile world, you will need to use the [Tiled Map Editor](https://www.mapeditor.org/) and afterwards [Import a Tile World](./import.html) to Unreal Engine in order to be able to use it in your project.

A Tile World is composed by the following classes:
- **[ATITileWorldActor](./atitileworldactor.html):** This is the actor that will be created when instancing a [Tile World](./utitileworld.html) asset, which contains a group of [Tile Map Components](../tilemaps/utitilemapcomponent.html) that takes care of rendering every [Tile Map Instances](./utitilemapinstance.html).

- **[UTITileWorld](./utitileworld.html):** This is the Tile World asset that was imported from Tiled and can only be modified from Tiled when importing or reimporting. 

- **[UTITileWorldInstance](../tiles/utitileworldinstance.html):** This is an instance of a [UTITileWorld](./utitileworld.html) that will get created when you add the asset to a level and can be modified at runtime (for example, by adding/removing maps)