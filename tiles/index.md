---
layout: default
---

[Home](../) / Tiles

# Tiles

## Table of Contents
- **[Custom Properties](./custom-properties.html)**
- **Classes**
  - **[UTITileMapTile](./utitilemaptile.html)**
  - **[UTITileMapTileInstance](./utitilemaptileinstance.html)**
  - **[UTITileSetTile](./utitilesettile.html)**
  - **[UTITileMapTileGroup](./utitilemaptilegroup.html)**

## Description
A Tile is a visual representation of an individual Tile Sprite stored in a [Tile Map](../tilemaps/index.md) or [Tile Set](../tilesets/index.md).

A Tile is composed by the following classes:
- **[UTITileMapTile](./utitilemaptile.html):** This is a individual Tile stored in a [Tile Map](../tilemaps/utitilemap.html) asset that was imported from Tiled and can only be modified from Tiled when importing or reimporting.

- **[UTITileMapTileInstance](./utitilemaptileinstance.html):** This is an instance of a [UTITileMapTile](./utitilemaptile.html) stored in a [Tile Map Instance](../tilemaps/utitilemapinstance.html) that will get created when you add a [Tile Map](./tilemaps/utitilemap.html) to a level and can be modified at runtime (for example, by adding/removing tiles)

- **[UTITileSetTile](./utitilesettile.html):** This an individual Tile stored in a [Tile Set](./tilesets/utitileset.md) that was imported from Tiled and can only be modified from Tiled when importing or reimporting.

- **[UTITileMapTileGroup](./utitilemaptilegroup.html):** This is a set of tiles in a [Tile Map Instance](../tilemaps/utitilemapinstance.html) grouped together by the `Group` ID Custom Property.