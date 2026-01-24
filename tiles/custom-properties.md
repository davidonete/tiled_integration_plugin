---
layout: default
---

[Home](../) / [Tiles](./index.md) / Custom Properties

## Tile Custom Properties
You can also specify some Unreal Engine properties for the Tiles within a Tile Set from Tiled, which will automatically set it on the imported asset.

Here is the list of custom properties that you can set up on your Tiles:

- **Opacity:** (float) Set this to change the Opacity of the Tile (a value between 0 and 1). (Semi transparency will only work on Translucent materials)

- **Group:** (int) Set this to create a [Tile Group](./utitilemaptilegroup.html) with all of the tiles with the same group id of this tile set.

- **UserDataName:** (string) Set this to set up the `UserData` property that can be used for pairing with Data Tables in Unreal.

- **ActorSpawnerID:** (string) The ID of the Actor to be spawned whenever this tile is used. (See [Tile Actor Spawner](./tile-actor-spawner.html) for more info)

- **ActorSpawnerOffsetX:** (float) The offset in the X axis from the center of the tile used for spawning the Actor. (See [Tile Actor Spawner](./tile-actor-spawner.html) for more info)

- **ActorSpawnerOffsetY:** (float) The offset in the Y axis from the center of the tile used for spawning the Actor. (See [Tile Actor Spawner](./tile-actor-spawner.html) for more info)

- **ActorSpawnerOffsetZ:** (float) The offset in the Z axis from the center of the tile used for spawning the Actor. (See [Tile Actor Spawner](./tile-actor-spawner.html) for more info)

A predefined set of Custom Properties is available to download and apply to your Tiled project, which includes all the above properties. You can set it up by following this guide:

**1.-** Download the predefined custom properties from [here](../custom-properties/tiled-custom-properties.json).

**2.-** Open the Custom Types Editor in `View > Custom Types Editor`, click on `Import` on the top right corner and select the previously downloaded file.

**3.-** To apply the properties to your tile, open the Tile Set and select a Tile, in the `Properties` window set the class to `Tile`. You should see new custom properties show for your tile.