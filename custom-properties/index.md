---
layout: default
---

[Home](../) / Custom Properties

## Custom Properties
Custom Properties is a feature from the Tiled Map Editor that allows you to store any kind of information on a [Tile Map](../tilemaps/index.md), [Tile Set](../tilesets/index.md), [Tile Layer](../tilelayers/index.md) or [Tiles](../tiles/index.md) for later use in your project. This plugin allows accessing this information from your Unreal Engine project at any moment either from Blueprints or from C++.

To access the Custom Properties of any of your Tile classes:

**1.-** Get a reference to the class placed in your level and use the `GetCustomProperties` method

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
You can also specify some Unreal Engine properties for Tile Maps, Tile Sets, Tile Layers and Tiles, which will automatically set it on the imported asset:

- [Tile Map Properties](../tilemaps/custom-properties.html)

- [Tile Set Properties](../tilesets/custom-properties.html)

- [Tile Layer Properties](../layers/custom-properties.html)

- [Tile Properties](../tiles/custom-properties.html)

A predefined set of Custom Properties is available to download and apply to your Tiled project, which includes all the above properties. You can set it up by following this guide:

**1.-** Download the predefined custom properties from [here](./tiled-custom-properties.json)

**2.-** Open the Custom Types Editor in `View > Custom Types Editor`, click on `Import` on the top right corner and select the previously downloaded file.