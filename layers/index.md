---
layout: default
---

[Home](../) / Tile Layers

# Tile Layers

## Table of Contents
- **Classes**
  - **[UTITileLayer](./utitilelayer.html)**
  - **[UTITileLayerInstance](./utitilelayerinstance.html)**

## Description
A Tile Layer is a visual representation of a group of [Tiles](../tiles/index.md) that are sorted within a [Tile Map](../tilemaps/index.md). The order of the layers detemine which tiles render first, where the lowest layers will render first and the higher layers last (on top of the lower layers). You can also override this order by using the `Elevation` Custom Property, (more info can be found [here](./custom-properties.html)

A Tile Layer is composed by the following classes:
- **[UTITileLayer](./utitilelayer.html):** This is the Tile Layer in a [Tile Map](../tilemaps/utitilemap.html) asset that was imported from Tiled and can only be modified from Tiled when importing or reimporting.

- **[UTITileLayerInstance](./utitilelayerinstance.html):** This is an instance of a [UTITileLayer](./utitilelayer.html) that will get created when you add the asset to a level and can be modified at runtime (for example, by adding/removing tiles)