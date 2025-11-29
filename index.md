---
layout: default
---

## Table of Contents
- **[Home](./)**
  - **[Description](./)**
  - **[Get in touch](./)**
  - **[Updates](./)**
- **[Getting Started](./getting-started.html)**
- **[Tile Maps](./tilemaps/index.md)**
  - **[Import a Tile Map](./tilemaps/import.html)**
  - **[Create a Blueprint](./tilemaps/blueprint.html)**
  - **[Custom Properties](./tilemaps/custom-properties.html)**
  - **Classes**
    - **[ATITileMapActor](./tilemaps/atitilemapactor.html)**
    - **[UTITileMap](./tilemaps/utitilemap.html)**
    - **[UTITileMapComponent](./tilemaps/utitilemapcomponent.html)**
    - **[UTITileMapInstance](./tilemaps/utitilemapinstance.html)**
- **[Tile Sets](./tilesets/index.md)**
  - **[Import a Tile Set](./tilesets/import.html)**
  - **[Custom Properties](./tilesets/custom-properties.html)**
  - **Classes**
    - **[UTITileSet](./tilesets/utitileset.html)**
	- **[UTITileSetTile](./tiles/utitilesettile.html)**
- **[Tile Layers](./layers/index.md)**
  - **[Custom Properties](./layers/custom-properties.html)**
  - **Classes**
	- **[UTITileLayer](./layers/utitilelayer.html)**
	- **[UTITileLayerInstance](./layers/utitilelayerinstance.html)**	
- **[Tiles](./tiles/index.md)**
  - **[Custom Properties](./tiles/custom-properties.html)**
  - **Classes**
    - **[UTITileMapTile](./tiles/utitilemaptile.html)**
    - **[UTITileMapTileInstance](./tiles/utitilemaptileinstance.html)**
    - **[UTITileSetTile](./tiles/utitilesettile.html)**
    - **[UTITileMapTileGroup](./tiles/utitilemaptilegroup.html)**
- **[Tile Worlds](./worlds/index.md)**
  - **[Import a Tile World](./worlds/import.html)**
  - **[Create a Blueprint](./worlds/blueprint.html)**
  - **Classes**
    - **[ATITileWorldActor](./worlds/atitileworldactor.html)**
    - **[UTITileWorld](./worlds/utitileworld.html)**
    - **[UTITileWorldInstance](./worlds/utitileworldinstance.html)**
- **[Custom Properties](./custom-properties/index.md)**
- **[Plugin Settings](./settings/index.md)**

## Description
This is a plugin for Unreal Engine 5 that simplifies the work of importing Tile Maps and Tile Sets made with [Tiled](https://www.mapeditor.org/). In addition it adds some quality time improvements and fixes to the original system. 

This is the complete list of features currently available:
* Import Tile Worlds
* Import Tile Maps
* Import Tile Sets
* Import Textures
* Auto Reimport
* Custom Properties
* Collisions
* Animated Tiles
* Modify Tile Maps at runtime
* Tile Grouping
* Normal maps
* Batch asset replace tool
* Batch modify sprite pivot point tool
* Batch flipbook extractor tool
* Blueprint support for Tile Map and Tile World actors

**Note:** This tool expects the user to use Tiled as the main Tile Map and Tile Set editor, completely replacing the Unreal Engine Tile Map and Tile Set editor. Doing changes such as modifying tiles, layers, collisions and/or dimensions directly into Unreal Engine is not supported and can lead to issues.

## Get in touch
If you find issues with the plugin please open a ticket [here](https://github.com/davidonete/tiled_integration_plugin/issues) with as much details as possible on what happened, how to reproduce and the expected result. We will look into it and reply back as soon as possible.

Alternatively you can join our [discord channel](https://discord.gg/C4eEcVgfmb) where you can report issues or request features, as well as ask for help or advice on related topics.

## Updates
### v1.14 (29/11/2025)
* Add custom data table row handle to remove the need of specifying the data table and allow them to be tmap keys
* Add begin play callback
* Upgrade to 5.7

### v1.13 (14/11/2025)
* Fix issues with blueprint tile map and tile world
* Fix resource loading issues
* Fix tile worlds not considering pixels per unreal units for positioning tile maps
* Add support to save and load presets for the flipbook extractor tool
* Fix custom properties not navigating correctly through subclasses
* Add support for copying custom properties from other custom properties
* Add support for customizing the class creation of all tiled classes
* Add template getters for ease of use of child classes
* Add support for layer visibility in game and in editor
* Fix browser extension tools not working on assets with child classes
* Regenerate tile world actors and blueprints when tile maps get reimported

### v1.12 (04/10/2025)
* Fix pivot point for flipbook extractor tool
* Add tile world support
* Fix plugin UI to allow multiple resources with the same name
* Allow creating tile map and tile world blueprints

### v1.11 (21/08/2025)
* Add sub elevation and separation per sub elevation custom properties
* Organize default custom properties
* Add helper library
* Allow changing layer visibility in runtime
* Enhance flipbook extractor tool to allow creating paper zd animations

### v1.10 (11/08/2025)
* Fix crash on calculating tile bounds
* Add support to use custom tile map tile group class
* Fix texture import crash
* Fix modify sprite pivot point tool
* Add flipbook extractor tool
* Add support for normal maps
* Allow manually importing texture
* Fix to prevent saving state before fully loading the resources

### v1.9 (26/07/2025)
* Add tile opacity transition feature
* Force reimport resources when pressing reimport button
* Add batch modify sprite pivot point tool
* Add batch asset replace tool
* Add tile bounds feature
* Add support for moving imported assets
* Add support for changing the imported source file

### v1.8 (14/07/2025)
* Prevent auto reimporting resources on loading
* Fix the postload method getting called before the object has actually loaded
* Fix bulk delete of resources issue
* Fix collisions not being generated at spawn time or when the tile map is modified
* Set the pivot point of sprites based on the tile map type
* Fix rotation for animated tiles
* Fix missing references on manually set up tile map components
* Prevent running the resource manager when packaging projects

### v1.7 (10/07/2025)
* Fix Tile Set Tiles custom properties not resetting properly
* Implement Tile Map Grouping
* Fix crash when deleting resource while being used in map
* Fix animated tiles rendering with wrong pivot point
* Replace SubElevation layer custom property with ElevationOffset
* Allow adding tile map assets to blueprints
* Add method to spawn tile maps on runtime

### v1.6 (27/06/2025)
* Upgrade to 5.6
* Fix player and visibility collision
* Add checks to prevent crashes when deleting assets
* Disable editor properties for tile maps, tile layers and tile sets
* Allow customizing the collision thickness and collision offset on tile maps and tile layers

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
