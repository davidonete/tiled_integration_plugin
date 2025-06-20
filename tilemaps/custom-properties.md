---
layout: default
---

[Home](../) / [Tile Maps](./index.html) / Custom Properties

## Custom Properties
Custom Properties is a feature from the Tiled Map Editor that allows you to store any kind of information on a Tile Map for later use in your project. This plugin allows accessing this information from your Unreal Engine project at any moment either from Blueprints or from C++.

To access the Custom Properties of your Tile Map:

**1.-** Get a reference to the `UTITileMapInstance` placed in your level and use the `GetCustomProperties` method

**2.-** From the `UTICustomProperties` class you will be able to access the Custom Properties by type:

  - **GetBoolProperty:** Tries to get the value of a boolean property by it's name, it will return false if the property is not found.
  
  - **GetNumberProperty:** Tries to get the value of a numeric property (int/double/float) by it's name, it will return false if the property is not found. This will also include enums saved as numbers.
  
  - **GetStringProperty:** Tries to get the value of a string property by it's name, it will return false if the property is not found.
  
  - **GetFileProperty:** Tries to get the value of a file property (as a string of the file path) by it's name, it will return false if the property is not found.
  
  - **GetColorProperty:** Tries to get the value of a color property by it's name, it will return false if the property is not found.
  
  - **GetClassProperty:** Tries to get the value of a class property by it's name, it will return false if the property is not found. A class can contain a group of more properties.
  
## Class Properties
When working with custom property classes it can get quite time consuming to get the class and then the property you want from code/blueprint, for that reason a shortcut system has been implement to access the properties under the classes directly. 

In order to do that you need to write the property name as the following format `ClassPropertyName.PropertyName` where:

- `ClassProperty` is the name of the class property.
- `PropertyName`  is the property name under the class property. You can specify as many `PropertyName`s as you want as long as they are sepparated with a dot.

E.g. Let's assume we have a class called `Point` which has two integers under it `X` and `Y`. In order to directly access `X` from the `Point` class, we would write the name of the property as `Point.X` on the getter method.

E.g.2. Let's assume we have a class `Shape` with the previous class `Point` inside. In order to directly access `X` from the `Shape` class, we would write the name of the property as `Shape.Point.X` on the getter method.

## Unreal Engine Properties
You can also specify some Unreal Engine properties for the Tile Map from Tiled, which will automatically set it on the imported asset.

Here is the list of custom properties that you can set up on your Tile Map:

- **PixelsPerUnrealUnit:** Set this to change the Pixels Per Unreal Unit setting on the Tile Map. (The scaling factor between pixels and Unreal units (cm) (e.g., 0.64 would make a 64 pixel wide tile take up 100 cm))

- **SeparationPerLayer:** Set this to change the Separation Per Layer setting on the Tile Map. (The Z-separation between each layer of the tile map)

- **SeparationPerTileX:** Set this to change the Separation Per Tile X setting on the Tile Map. (The Z-separation incurred as you travel in X)

- **SeparationPerTileY:** Set this to change the Separation Per Tile Y setting on the Tile Map. (The Z-separation incurred as you travel in Y)

- **SeparationPerElevation:** Value to determine how separated (in the Z axis) are the layers based of the Elevation custom property.

- **SeparationPerSubElevation:** Value to determine how separated (in the Z axis) are the layers based of the SubElevation custom property.

A predefined set of Custom Properties is available to download and apply to your Tiled project, which includes all the above properties. You can set it up by following this guide:

**1.-** Download the predefined custom properties from [here](https://davidonete.github.io/tiled_integration_plugin/assets/other/tiled-custom-properties.json)

**2.-** Open the Custom Types Editor in `View > Custom Types Editor`, click on `Import` on the top right corner and select the previously downloaded file.

**3.-** To apply the properties to your map, open the Tile Map Properties in `Map > Map Properties` and set the class to `Map`. You should see new custom properties show for your map.