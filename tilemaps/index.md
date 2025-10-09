---
layout: default
---

[Home](../) / Tile Maps

# Tile Maps

## Table of Contents
- **[Import a Tile Map](./import.html)**
- **[Create a Blueprint](./blueprint.html)**
- **[Custom Properties](./custom-properties.html)**
- **Classes**
  - **[ATITileMapActor](./atitilemapactor.html)**
  - **[UTITileMap](./utitilemap.html)**
  - **[UTITileMapComponent](./utitilemapcomponent.html)**
  - **[UTITileMapInstance](./utitilemapinstance.html)**

## Description
A Tile Map is a visual representation of a group of [Tiles](../tiles/index.md) organized within [Tile Layers](../layers/index.md). To create and modify a tile map, you will need to use the [Tiled Map Editor](https://www.mapeditor.org/) and afterwards [Import a Tile Map](./import.html) to Unreal Engine in order to be able to use it in your project.

A Tile Map is composed by the following classes:
- **[ATITileMapActor](./atitilemapactor.html):** This is the actor that will be created when instancing a [Tile Map](./utitilemap.html) asset, which contains a [Tile Map Component](./utitilemapcomponent.html) that takes care of rendering the [Tile Map Instance](./utitilemapinstance.html).

- **[UTITileMap](./utitilemap.html):** This is the Tile Map asset that was imported from Tiled and can only be modified from Tiled when importing or reimporting.

- **[UTITileMapComponent](./utitilemapcomponent.html):** This is the component that takes care of rendering the [Tile Map Instance](./utitilemapinstance.html) and is part of a [Tile Map Actor](./atitilemapactor.html).

- **[UTITileMapInstance](./utitilemapinstance.html):** This is an instance of a [UTITileMap](./utitilemap.html) that will get created when you add the asset to a level and can be modified at runtime (for example, by adding/removing tiles)