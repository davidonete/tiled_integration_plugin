---
layout: default
---

[Home](../) / Plugin Settings

## Plugin Settings

You can configure some aspects of the plugin to adjust it better to your needs. The configuration can be found in `Edit > Project Settings > Plugins > Tiled Integration`.
Here are the options that you can configure:

- **Save File Path:** Where the plugin save file will be located relative to your project directory. By default it will be located in the root folder of your project. **Note:** If you change the location in the settings you must also manually change the file location accordingly and restart the engine.
  
- **Tile Map Class:** The class that will be used when importing a Tile Map asset. If you want to use your own class it must inherit from **[UTITileMap](../tilemaps/utitilemap.html)**. **Note:** Changing this after importing assets is not supported, please remove all imported assets before changing it and reimport them afterwards.

- **Tile Map Instance Class:** The class that will be used when creating a Tile Map asset. If you want to use your own class it must inherit from **[UTITileMapInstance](../tilemaps/utitilemapinstance.html)**. **Note:** Changing this after importing assets is not supported, please remove all imported assets before changing it and reimport them afterwards.

- **Tile Map Actor Class:** The class that will be used when instancing a Tile Map asset into a level. If you want to use your own class it must inherit from **[ATITileMapActor](../tilemaps/atitilemapactor.html)**. **Note:** Changing this after importing assets is not supported, please remove all imported assets before changing it and reimport them afterwards.
  
- **Tile Set Class:** The class that will be used when importing a Tile Set asset. If you want to use your own class it must inherit from **[UTITileSet](../tilesets/utitileset.html)**. **Note:** Changing this after importing assets is not supported, please remove all imported assets before changing it and reimport them afterwards.
  
- **Tile Layer Class:** The class that will be used when importing a Tile Layer from a Tile Map asset. If you want to use your own class it must inherit from **[UTITileLayer](../layers/utitilelayer.html)**. **Note:** Changing this after importing assets is not supported, please remove all imported assets before changing it and reimport them afterwards.
  
- **Tile Layer Class:** The class that will be used when creating a Tile Layer from a Tile Map asset. If you want to use your own class it must inherit from **[UTITileLayerInstance](../layers/utitilelayerinstance.html)**. **Note:** Changing this after importing assets is not supported, please remove all imported assets before changing it and reimport them afterwards.
  
- **Tile Map Tile Class:** The class that will be used to represent a single tile within a Tile Map. If you want to use your own class it must inherit from **[UTITileMapTile](../tiles/utitilemaptile.html)**. **Note:** Changing this after importing assets is not supported, please remove all imported assets before changing it and reimport them afterwards.

- **Tile Map Tile Instance Class:** The class that will be used to create a tile instance from a Tile Map asset. If you want to use your own class it must inherit from **[UTITileMapTileInstance](../tiles/utitilemaptileinstance.html)**. **Note:** Changing this after importing assets is not supported, please remove all imported assets before changing it and reimport them afterwards.

- **Tile Set Tile Class:** The class that will be used to represent a tile within a Tile Set. If you want to use your own class it must inherit from **[UTITileSetTile](../tiles/utitilesettile.html)**. **Note:** Changing this after importing assets is not supported, please remove all imported assets before changing it and reimport them afterwards.

- **Tile Map Naming Convention:** The naming convention of the Tile Map assets generated when importing, where {0} is the name of the original Tile Map file.

- **Tile Set Naming Convention:** The naming convention of the Tile Set assets generated when importing, where {0} is the name of the original Tile Set file.

- **Tile Set Texture Naming Convention:** The naming convention of the Tile Set Textures assets generated when importing, where {0} is the name of the original Texture file.

- **Tile Set Flipbook Naming Convention:** The naming convention of the Tile Set Flipbooks assets generated when importing, where {0} is the name of the Tile Set file and {1} is the ID of the Tile.

- **Tile Set Sprite Naming Convention:** The naming convention of the Tile Set Sprites assets generated when importing, where {0} is the name of the Tile Set file and {1} is the ID of the Tile.

![Plugin Settings](https://davidonete.github.io/tiled_integration_plugin/assets/images/tiled_integration_plugin/plugin_settings.jpg)