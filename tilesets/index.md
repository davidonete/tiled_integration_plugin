---
layout: default
---

[Home](../) / Tile Sets

# Tile Sets

## Table of Contents
- **[Import a Tile Set](./import.html)**
- **[Custom Properties](./custom-properties.html)**
- **Classes**
  - **[UTITileSet](./utitileset.html)**
  - **[UTITileSetTile](../tiles/utitilesettile.html)**
  
## Description

A Tile Set is a collection of individual [Tiles](../tiles/utitilesettile.html) placed in a tile sheet image, and are used to create [Tile Maps](../tilemaps/index.md). To create and modify a tile set, you will need to use the [Tiled Map Editor](https://www.mapeditor.org/) and afterwards [Import a Tile Set](./import.html) to Unreal Engine in order to be able to use it in your project.

A Tile Set is composed by the following classes:
- **[UTITileSet](./utitileset.html):** This is the Tile Set asset that was imported from Tiled which contain a list of [Tile Set Tiles](../tiles/utitilesettile.html) and can only be modified from Tiled when importing or reimporting. 

- **[UTITileSetTile](../tiles/utitilesettile.html):** This is the class representing an individual Tile inside a Tile Set.