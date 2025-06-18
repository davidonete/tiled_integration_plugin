---
layout: default
---

[Home](../) / Tile Maps

# Tile Maps

## Table of Contents
- [Tile Maps](./index.html)
  - [Import a Tile Map](./import.html)
  - [Custom Properties](./custom-properties.html)
  - [Functions](./functions.html)

## Description
A Tile Map is a visual representation of a group of [Tiles](../tiles/index.html) organized within [Tile Layers](../layers/index.html). To create and modify a tile map, we will use the [Tiled map editor](https://www.mapeditor.org/) and afterwards [import the map](./import.html) to Unreal Engine in order to be able to use it in your project.

Within the engine, we can find two types of Tile Maps:
- **UTITileMap:** This is the Tile Map asset that was imported from Tiled and can only be modified from Tiled.
- **UTITileMapInstance:** This is an instance of a ``UTITileMap`` that will get created when you add the asset to a level and can be modified at runtime (for example, by adding/removing tiles)

**Note:** If you want to extend the above classes either via C++ or Blueprint, you can specify in the [Plugin settings](../settings/index.md) what classes the plugin should use, instead of the default ones (your classes must be child classes from the ones you want to replace).