---
layout: default
---

[Home](../) / [Tile Layers](./index.md) / Custom Properties

## Tile Layer Custom Properties
You can specify some Unreal Engine properties for the Tile Layer from Tiled, which will automatically set it on the imported asset.

Here is the list of custom properties that you can set up on your Tile Layer:

- **CollisionEnabled:** (bool) Set this to enable/disable the collisions for this particular layer. (By default collisions are enabled)

- **CollisionOffset:** (float) Set this to add a height offset to the generated collision shape.

- **CollisionThickness:** (float) Set this specify the thickness of the generated collision shape for this layer (By default the collision thickness is 50 units)

- **Elevation:** (int) Set this to override the rendering order of the layer (the higher the value the closer it will be to the camera) (if you set this on one layer you should set it of all the other layers too) (By default the order is determined by the layer order in Tiled)

- **ElevationOffset:** (float) Set this to add an height offset from the specified `Elevation`. It's recommended to use this to avoid Z-fighting when setting multiple layers to the same `Elevation`.

- **VisibleInGame:** (bool) Set this to enable/disable visibility of the layer in the game.

- **VisibleInEditor:** (bool) Set this to enable/disable visibility of the layer in the editor.

A predefined set of Custom Properties is available to download and apply to your Tiled project, which includes all the above properties. You can set it up by following this guide:

**1.-** Download the predefined custom properties from [here](../custom-properties/tiled-custom-properties.json)

**2.-** Open the Custom Types Editor in `View > Custom Types Editor`, click on `Import` on the top right corner and select the previously downloaded file.

**3.-** To apply the properties to your layer, select the layer you want on the layer tab and set the class to `Layer`. You should see new custom properties show for your layer.
