---
layout: default
---

## Table of Contents
1. [Home](./)
  - [Description](./)
  - [Get in touch](./)
  - [Updates](./)
2. [Getting Started](./getting-started.html)
3. [Tile Maps](./tilemaps/index.md)
  - [Import a Tile Map](./tilemaps/import.html)
  - [Custom Properties](./tilemaps/custom-properties.html)
  - Classes
	  - [UTITileMap](./tilemaps/utitilemap.html)
	  - [UTITileMapInstance](./tilemaps/utitilemapinstance.html)
4. [Tile Sets](./tilesets/index.md)
  - [Import a Tile Set](./tilesets/import.html)
  - [Custom Properties](./tilesets/custom-properties.html)
  - [Functions](./tilesets/functions.html)
5. [Tile Layers](./layers/index.md)
  - Classes
	  - [UTITileLayer](./layers/utitilelayer.html)
	  - [UTITileLayerInstance](./layers/utitilelayerinstance.html)	
6. [Tiles](./tiles/index.md)
  - Classes
	  - [UTITileMapTile](./tiles/utitilemaptile.html)
	  - [UTITileMapTileInstance](./tiles/utitilemaptileinstance.html)	
	  - [UTITileSetTile](./tiles/utitilesettile.html)
7. [Tile Map Component](./component/index.md)
8. [Tile Map Actor](./actor/index.md)
9. [Custom Properties](./custom-properties/index.md)
10. [Plugin Settings](./settings/index.md)

## Description
This is a plugin for Unreal Engine 5 that simplifies the work of importing Tile Maps and Tile Sets made with [Tiled](https://www.mapeditor.org/). In addition it adds some quality time improvements and fixes to the original system. 

This is the complete list of features currently available:
* Import Tiled Tile Maps
* Import Tiled Tile Sets (and textures)
* Auto Reimport feature when modified from Tiled
* Support for Custom Properties for Tile Maps, Tile Sets, Layers and Tiles
* Support for setting up Collisions from Tiled
* Support for Animated Tiles

**Note:** This tool expects the user to use Tiled as the main Tile Map and Tile Set editor, completely replacing the Unreal Engine Tilemap and Tileset editor. Doing changes such as modifying tiles, layers, collisions and/or dimensions directly into Unreal Engine is not supported and can lead to issues.

## Get in touch
If you find issues with the plugin please open a ticket [here](https://github.com/davidonete/tiled_integration_plugin/issues) with as much details as possible on what happened, how to reproduce and the expected result. We will look into it and reply back as soon as possible.

Alternatively you can join our [discord channel](https://discord.gg/C4eEcVgfmb) where you can report issues or request features, as well as ask for help or advice on related topics.

## Updates
### v1.5 (17/06/2025)
* Add support for changing the tile maps at runtime
* Allow infinite tile maps
* Add option to condition tile set textures at import time
* Simplify deletion of imported resources
* Add filters to the UI to help searching for imported tile maps and tile sets

### v1.4 (22/05/2025)
* Fix error calculating bounds on maps with only one layer
* Add default separation per tile for isometric maps and invert it's value

### v1.3 (29/04/2025)
* Add on instanced callbacks and save owner tile map actor when spawned
* Fix importing standalone tilesets incorrectly flagged as embedded
* Fix issue duplicating tile set when already imported
* Save last imported time to prevent reimporting when relaunching the engine
* Add SubElevation and fix render order for translucent materials
* Fix layer becoming invalid when tileset gets reimported
* Fix issue reimporting a tile map with multiple tile sets
* Add opacity custom property for tile and tile instance and fix crash on invalid tile pointer in tile instance not saving correctly
* Expose generated files naming conventions

### v1.2 (09/10/2024)
* Add support for UE 5.5
* Fix bounding box not generating correctly
* Add Elevation custom property to tile layers
* Move plugin settings to project settings
* Fix material being overriden when reimporting
