---
layout: default
---

[Home](../) / [Tile Maps](./index.md) / Custom Properties

## Tile Map Custom Properties
You can also specify some Unreal Engine properties for the Tile Map from Tiled, which will automatically set it on the imported asset.

Here is the list of custom properties that you can set up on your Tile Map:

- **PixelsPerUnrealUnit:** Set this to change the Pixels Per Unreal Unit setting on the Tile Map. (The scaling factor between pixels and Unreal units (cm) (e.g., 0.64 would make a 64 pixel wide tile take up 100 cm))

- **SeparationPerLayer:** Set this to change the Separation Per Layer setting on the Tile Map. (The Z-separation between each layer of the tile map)

- **SeparationPerTileX:** Set this to change the Separation Per Tile X setting on the Tile Map. (The Z-separation incurred as you travel in X)

- **SeparationPerTileY:** Set this to change the Separation Per Tile Y setting on the Tile Map. (The Z-separation incurred as you travel in Y)

- **SeparationPerElevation:** Value to determine how separated (in the Z axis) are the layers based of the Elevation custom property.

- **SeparationPerSubElevation:** Value to determine how separated (in the Z axis) are the layers based of the SubElevation custom property.

- **CollisionThickness:** The extrusion thickness of collision geometry when using a 3D collision domain.

A predefined set of Custom Properties is available to download and apply to your Tiled project, which includes all the above properties. You can set it up by following this guide:

**1.-** Download the predefined custom properties from [here](../custom-properties/tiled-custom-properties.json)

**2.-** Open the Custom Types Editor in `View > Custom Types Editor`, click on `Import` on the top right corner and select the previously downloaded file.

**3.-** To apply the properties to your map, open the Tile Map Properties in `Map > Map Properties` and set the class to `Map`. You should see new custom properties show for your map.