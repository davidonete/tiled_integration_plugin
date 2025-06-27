---
layout: default
---

[Home](../) / Tile Maps

# Tile Maps

## Table of Contents
- **[Import a Tile Map](./import.html)**
- **[Custom Properties](./custom-properties.html)**
- **Classes**
  - **[UTITileMap](./utitilemap.html)**
  - **[UTITileMapInstance](./utitilemapinstance.html)**

## Description
A Tile Map is a visual representation of a group of [Tiles](../tiles/index.md) organized within [Tile Layers](../layers/index.md). To create and modify a tile map, you will need to use the [Tiled Map Editor](https://www.mapeditor.org/) and afterwards [Import a Tile Map](./import.html) to Unreal Engine in order to be able to use it in your project.

In the plugin there are two kind of Tile Maps classes:

- **[UTITileMap](./utitilemap.html):** This is the Tile Map asset that was imported from Tiled and can only be modified from Tiled when importing or reimporting.

- **[UTITileMapInstance](./utitilemapinstance.html):** This is an instance of a `UTITileMap` that will get created when you add the asset to a level and can be modified at runtime (for example, by adding/removing tiles)