---
layout: default
---

## Description

This is a plugin for Unreal Engine 5 that simplifies the work of importing Tile Maps and Tile Sets made with [Tiled](https://www.mapeditor.org/). In addition it adds some quality time improvements and fixes from the default importer that came with Unreal Engine by default. 

This is the complete list of features currently available:

* Import Tiled Tile Maps
* Import Tiled Tile Sets (and textures)
* Auto Reimport assets when modified from Tiled
* Support for Custom Properties for Tile Maps, Tile Sets, Layers and Tiles
* Fix to allow importing Tile Collisions from Tiled
* Animated Tiles
* Some Unreal Engine configuration exposed to be set up from Tiled.

[Quick Video Guide](https://www.youtube.com/watch?v=AQnpu9husAo)

**Note:** This tool expects the user to use Tiled as the main Tile Map and Tile Set editor, doing changes such as modifying tiles, layers, collisions and/or dimensions directly into Unreal Engine can lead to unexpected behavior and it is not recommended.

## How to Use
**1.-** Get the plugin from the [Unreal Engine Marketplace](https://www.unrealengine.com/marketplace/en-US/product/7cde7c5f731743888f4068c8e8c24f6a) and install it into your Unreal Engine version via the Epic Games Launcher.

**2.-** Create a new project or open an existing one and activate the plugin in Edit > Plugins > TiledIntegration. You will have to restart Unreal Engine afterwards.

![Activate plugin](https://davidonete.github.io/tiled_integration_plugin/assets/images/tiled_integration_plugin/activate_plugin.jpg)

**3.-** After restarting Unreal Engine, you should see a new icon on the toolbar next to the play button. 

![New button](https://davidonete.github.io/tiled_integration_plugin/assets/images/tiled_integration_plugin/new_button.jpg)

**4.-** If you click it it should open the Control Panel from where you will be able to manage the Tiled Resources.

![Control Panel](https://davidonete.github.io/tiled_integration_plugin/assets/images/tiled_integration_plugin/control_panel.jpg)

**5.-** To get started simply click on the Import button at the bottom and look for a Tiled Tile Map or Tile Set file to import.
   
**Note:** The file to be imported must be saved as a JSON file in Tiled.

**Note:** When importing a Tile Map and Tile Sets it will also import it's dependencies (Tile Set and/or Textures)

**Note:** The plugin comes with some example files that you can try located in "\<Unreal Engine Installation Folder\>/Engine/Plugins/Marketplace/TiledIntegration/ExampleTiledFiles" (e.g. "C:\Program Files\Epic Games\UE_5.4\Engine\Plugins\Marketplace\TiledIntegration\Content\ExampleTiledFiles")

![Pick asset](https://davidonete.github.io/tiled_integration_plugin/assets/images/tiled_integration_plugin/pick_asset.jpg)

**6.-** After picking the file to import you will be requested to specify the place where you want the asset to be imported to and which name you want to set. Please pick a location that is within your project content folder. You can see on the title of the window what kind of asset you want to save.

**Note:** Please pick a definitive name and location as **MOVING** or **RENAMING** the asset after it has been imported is not supported and you will need to start the process again if so.

![Pick asset](https://davidonete.github.io/tiled_integration_plugin/assets/images/tiled_integration_plugin/save_asset.jpg)

**7.-** If everything went well, you should see your imported assets in the place where you specified it as well as a new dropdown option on the Control Panel from where you can manage your imported assets. From this menu you will be able to do the following:
   - **Status:** Check if the asset or the file has any issues.
   - **Asset Location:** See and navigate to the location of the Unreal Engine Asset.
   - **Source Location:** See and navigate to the location of the Tiled Asset.
   - **Auto Reimport:** Set if the plugin should reimport the Tiled Asset when it detects a change.
   - **Dependencies:** Check the list of Tiled Assets that the selected asset depends on.
   - **Used By:** Check the list of Tiled Assets that use the selected asset.
   - **Reimport:** Manually reimport the selected asset.
   - **Refresh:** Refresh the information in the Control Panel.
   - **Delete:** Delete the selected asset from Unreal Engine and it's dependencies.

![Pick asset](https://davidonete.github.io/tiled_integration_plugin/assets/images/tiled_integration_plugin/imported_assets.jpg)

## Custom Properties
In order to support Tiled Custom Properties on Tile Maps, Tile Sets, Tiles and Layers, we have extended the default Paper2D classes to support this. We will explain how to access this classes from Blueprints and from C++ in the following sections.

### Tile Map Custom Properties
#### Unreal Engine Variables
You can define the following Custom Properties in the Tiled Tile Map which will be used in Unreal Engine when imported:
* **PixelsPerUnrealUnit:** Set this to change the Pixels Per Unreal Unit setting on the Tile Map. (The scaling factor between pixels and Unreal units (cm) (e.g., 0.64 would make a 64 pixel wide tile take up 100 cm))
  
* **SeparationPerLayer:** Set this to change the Separation Per Layer setting on the Tile Map. (The Z-separation between each layer of the tile map)

* **SeparationPerTileX:** Set this to change the Separation Per Tile X setting on the Tile Map. (The Z-separation incurred as you travel in X)

* **SeparationPerTileY:** Set this to change the Separation Per Tile Y setting on the Tile Map. (The Z-separation incurred as you travel in Y)

#### Blueprint
In order to access the Custom Properties of a Tile Map from blueprint you just need a reference to your Paper Tile Map Actor that is placed in your level and use the method that we provided ``Get Tile Map From Actor``. From there you can use ``Get Custom Properties`` method and get the property you want by name and type.

![Tile Map Custom Properties Blueprint](https://davidonete.github.io/tiled_integration_plugin/assets/images/tiled_integration_plugin/tile_map_custom_properties_blueprint.jpg)

#### C++
From C++ the process is very similar. You will need a reference to the Paper Tile Map Actor and call the helper method ``GetTileMapFromActor`` from ``UTiledIntegrationTileMapLibrary`` located in ``TiledIntegrationTileMap.h`` or you can directly cast from ``UPaperTileMap`` to ``UTiledIntegrationTileMap`` and use the ``GetCustomProperties`` method to access the properties. 

If you want to use a custom class for Tile Maps you can inherit from our ``UTiledIntegrationTileMap`` class and remember to change the default class type in the Plugin Configuration (explained in a section below).

### Tile Layer Custom Properties
#### Unreal Engine Variables
You can define the following Custom Properties in the Tiled Tile within the Tile Layer which will be used in Unreal Engine when imported:
* **Elevation:** This will determine how high (closer to the camera) the layer is and will be used by the system to sort it accordingly. If nothing is specified the layer order will be used to sorting.

#### Blueprint
There are multiple options available for accessing a Tile Layer Custom Properties:
* Use the ``Get Tile Layer From Actor`` method which requires a reference to the Paper Tile Map Actor placed in your level, and use ``Get Custom Properties`` method and get the property you want by name and type.
  
* Use the ``Get Layer`` or ``Get Layers By Name`` method from the Tiled Integration Tile Map which is returned by the ``Get Tile Map From Actor`` method explained above, and use ``Get Custom Properties`` method and get the property you want by name and type.

**Note:** The Layer Index is the identifier of the layer in your Tile Map that goes from 0 for the very first layer starting from the top of the list up to the amount of layers - 1.

![Tile Layer Custom Properties Blueprint](https://davidonete.github.io/tiled_integration_plugin/assets/images/tiled_integration_plugin/tile_layer_custom_properties_blueprint.jpg)

#### C++
There are multiple options available for accessing a Tile Layer Custom Properties:
* Use the helper method method ``GetTileLayerFromActor`` from ``UTiledIntegrationTileMapLibrary`` located in ``TiledIntegrationTileMap.h`` and then use the ``GetCustomProperties`` method to access the custom properties.
  
* Use the ``GetLayer`` or ``GetLayerByName`` method in ``UTiledIntegrationTileMap`` and then use the ``GetCustomProperties`` method to access the custom properties.

If you want to use a custom class for Tile Layers you can inherit from our ``UTiledIntegrationTileLayer`` class and remember to change the default class type in the Plugin Configuration (explained in a section below).

### Tile Custom Properties
#### Unreal Engine Variables
You can define the following Custom Properties in the Tiled Tile within the TileSet which will be used in Unreal Engine when imported:
* **UserDataName:** Set this to change the User Data Name on a individual Tile  in a Tile Set. (A tag that can be used for grouping and categorizing (consider using it as the index into a UDataTable asset))
  
#### Blueprint
In order to access the Custom Properties of a Tile from blueprint you just need a reference to your Paper Tile Map Actor that is placed in your level and use the method that we provided ``Get Tile Map From Actor``. From there you will need to retrieve the Layer by it's index using ``Get Layer`` and after that use `` can use ``Get Tile Custom Properties`` specifying the X and Y coordinates of the tile you want from that layer.

**Note:** The Layer Index is the identifier of the layer in your Tile Map that goes from 0 for the very first layer starting from the top of the list up to the amount of layers - 1.

**Note:** If the given Tile coordinates don't contain any Tiles or if the Tile doesn't have any Custom Properties ``Get Tile Custom Properties`` will retrun null.

![Tile Custom Properties Blueprint](https://davidonete.github.io/tiled_integration_plugin/assets/images/tiled_integration_plugin/tile_custom_properties_blueprint.jpg)

#### C++
For accessing a Tile Custom Properties get the Layer from one of the methods explained above and then use the ``GetTileCustomProperties`` method to access the custom properties.

### Tile Set Custom Properties
#### Blueprint
There are multiple options available for accessing a Tile Layer Custom Properties:
* Use the ``Get Tile Set From Actor`` method which requires a reference to the Paper Tile Map Actor placed in your level, the X and Y coordinates of the Tile and the Layer Index. Then use ``Get Custom Properties`` method and get the property you want by name and type.
  
* Use the ``Get Tile Set`` method from the Tiled Integration Tile Map which is returned by the ``Get Tile Map From Actor`` method explained above, and use ``Get Custom Properties`` method and get the property you want by name and type.

**Note:** The Layer Index is the identifier of the layer in your Tile Map that goes from 0 for the very first layer starting from the top of the list up to the amount of layers - 1.

**Note:** If the given Tile coordinates don't contain any Tiles ``Get Tile Set`` will retrun null.

![Tile Set Custom Properties Blueprint](https://davidonete.github.io/tiled_integration_plugin/assets/images/tiled_integration_plugin/tile_set_custom_properties_blueprint.jpg)

#### C++
There are multiple options available for accessing a Tile Set Custom Properties:
* Use the helper method method ``GetTileSetFromActor`` from ``UTiledIntegrationTileMapLibrary`` located in ``TiledIntegrationTileMap.h`` and then use ``GetCustomProperties`` to access the custom properties.
  
* Use the ``GetTileSet`` method in ``UTiledIntegrationTileMap`` and then use ``GetCustomProperties`` to access the custom properties.
  
* Get the Layer from one of the methods explained above and then use the ``GetTileSet`` method  and ``GetCustomProperties`` to access the custom properties.

### Tile Instance Custom Properties
A tile instance is a unique tile in the tile map (not to be confused with the tile in the tilesets). Due to Tiled limitation you will need to place the custom properties of the tile instance within the tile map custom properties as a class with the following naming format ``TileProperties[X,Y,Z]``, where X and Y are the coordinates of the tile within the tile map and Z the layer index (where 0 is the highest layer). If done correctly the properties will be transferred to the UTITileInstance when importing the tile map.

### Class Property Shortcuts
When you work with custom property classes it can get quite time consuming to get the class and then the property you want from code/blueprint, so I have created a shortcut system where you can access the properties under the classes directly. In order to do that you need to write the property name as the following format ``ClassPropertyName.PropertyName`` where ClassProperty is the name of the class property and sepparated by a dot you can write the names of the properties that are under the class. 

E.g. Let's assume we have a class called Point which has two integers under it X and Y. In order to directly access X from the Point class we would write the name as ``Point.X`` on the getter method.

## Collisions
You can add collisions to specific tiles by using the [Tiled Collision Editor](https://doc.mapeditor.org/en/stable/manual/editing-tilesets/#id2) tool. The supported collision types are Rectangles, Ellipses and Polygons.

**Note:** Rotations are not supported at the moment.

**Note:** Ellipses must be in the shape of circles (same width and height).

## Animated Tiles
You can add animated tiles to your Tile Set and Tile Map by using the [Tiled Animation Editor](https://doc.mapeditor.org/en/stable/manual/editing-tilesets/#id3) tool and placing the animated tile into your Tile Map.

**Note:** Placing many animated tiles in very big Tile Maps can become costly quite quickly. It is recommended that you keep the tile maps as small as possible (ideally combine small tile maps together to make a big one and show/hide them when needed)

## Plugin Configuration
You can configure some aspects of the plugin to adjust it better to your needs. The configuration can be found in Edit > Editor Preferences > Tiled Integration.
Here are the options that you can configure:
* **Save File Path:** Where the plugin save file will be located relative to your project directory. By default it will be located in the root folder of your project. **Note:** If you change the location in the settings you must also manually change the file location accordingly and restart the engine.
  
* **Tile Map Class:** The C++ class that will be used when importing a Tile Map asset. If you want to use your own class it must inherit from ``UTiledIntegrationTileMap``. **Note:** Changing this after importing assets is not supported, please remove all imported assets before changing it and reimport them afterwards.
  
* **Tile Set Class:** The C++ class that will be used when importing a Tile Set asset. If you want to use your own class it must inherit from ``UTiledIntegrationTileSet``. **Note:** Changing this after importing assets is not supported, please remove all imported assets before changing it and reimport them afterwards.
  
* **Tile Layer Class:** The C++ class that will be used when importing a Tile Layer from a Tile Map asset. If you want to use your own class it must inherit from ``UTiledIntegrationTileLayer``. **Note:** Changing this after importing assets is not supported, please remove all imported assets before changing it and reimport them afterwards.

![Plugin Settings](https://davidonete.github.io/tiled_integration_plugin/assets/images/tiled_integration_plugin/plugin_settings.jpg)

## Contact
If you find issues with the plugin please open a ticket [here](https://github.com/davidonete/tiled_integration_plugin/issues) with as much details as possible on what happened, how to reproduce and the expected result. We will look into it and reply back as soon as possible.
