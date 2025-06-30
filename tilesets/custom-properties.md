---
layout: default
---

[Home](../) / [Tile Sets](./index.md) / Custom Properties

## Tile Set Custom Properties
You can also specify some Unreal Engine properties for the Tile Set from Tiled, which will automatically set it on the imported asset.

Here is the list of custom properties that you can set up on your Tile Set:

- **ConditionTexture:** Conditions the tile sheet texture for the selected tile set by duplicating tile edges to create a buffer zone around each tile. (Same as `Right Click > Condition Tile Sheet Texture`).

- **ExtrusionAmount:** The amount to extrude out from the edge of each tile (in pixels) when conditioning the texture.

- **FillWithTransparentBlack:** Should we use transparent black or white when filling the texture areas that aren't covered by tiles when conditioning the texture.

- **PadToPowerOf2:** Should we pad the conditioned texture to the next power of 2 when conditioning the texture.

A predefined set of Custom Properties is available to download and apply to your Tiled project, which includes all the above properties. You can set it up by following this guide:

**1.-** Download the predefined custom properties from [here](../custom-properties/tiled-custom-properties.json)

**2.-** Open the Custom Types Editor in `View > Custom Types Editor`, click on `Import` on the top right corner and select the previously downloaded file.

**3.-** To apply the properties to your Tile Set, open the Tile Set Properties and set the class to `TileSet`. You should see new custom properties show for your Tile Set.