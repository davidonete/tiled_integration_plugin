---
layout: default
---

[Home](../) / [Tile Worlds](./index.md) / Create a Blueprint

## Create a Blueprint
**1.-** The first step is to import your [Tile World](./utitileworld.html) asset, to do that pleasae follow the guide in [Import a Tile World](./import.html).

**2.-** Once you have the [Tile World](./utitileworld.html) asset ready, we can create a blueprint instance for it using one of the following methods

- ```Right Click on the asset``` > ```Tiled Integration``` > ```Create Blueprint```

- Create a actor blueprint with the [ATITileWorldActor](./atitileworldactor.html) class or a children class from it, then open the blueprint and select the ```Root``` and set the ```Tile World``` property to use the asset you want and finally compile and save.

**Note:** Changing the ```Tile World``` property from the blueprint won't update the preview window, to force an update, close and reopen the blueprint editor.

**Note:** Do not add a [Tile Map Component](../tilemaps/utitilemapcomponent.html) manually to any blueprints as it is not supported and will have unexpected behavior.