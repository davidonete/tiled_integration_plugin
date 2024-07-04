---
layout: default
---

# Tiled Integration Plugin

## Description

This is a plugin for Unreal Engine 5 that simplifies the work of importing Tile Maps and Tile Sets made with [Tiled](https://www.mapeditor.org/). In addition it adds some quality time improvements and fixes from the default importer that came with Unreal Engine by default. 

This is the complete list of features currently available:

* Import Tiled Tile Maps
* Import Tiled Tile Sets (and textures)
* Auto Reimport when modified from Tiled
* Support for Custom Properties for Tile Maps, Tile Sets, Layers and Tiles
* Fix to allow importing Tile Collisions from Tiled

## How to Use
1.- Purchase the plugin from the [Unreal Engine Marketplace](https://www.unrealengine.com/marketplace/en-US/store) and install it into your Unreal Engine version via the Epic Games Launcher.

2.- Create a new project or open an existing one and activate the plugin in Edit > Plugins > TiledIntegration. You will have to restart Unreal Engine afterwards.

![Activate plugin](https://davidonete.github.io/assets/images/tiled_integration_plugin/activate_plugin.jpg)

3.- After restarting Unreal Engine, you should see a new icon on the toolbar next to the play button. 

![New button](https://davidonete.github.io/assets/images/tiled_integration_plugin/new_button.jpg)

4.- If you click it it should open the Control Panel from where you will be able to manage the Tiled Resources.

![Control Panel](https://davidonete.github.io/assets/images/tiled_integration_plugin/control_panel.jpg)

5.- To get started simply click on the Import button at the bottom and look for a Tiled Tile Map or Tile Set. It will ask you for the Tiled Tile Map or Tile Set to import.
   
**Note:** The file to be imported must be saved as a JSON file in Tiled.

**Note:** When importing a Tile Map and Tile Sets it will also import it's dependencies (Tile Set and/or Textures)

**Note:** The plugin comes with some example files that you can try located in "\<Unreal Engine Installation Folder\>/Engine/Plugins/TiledIntegration/ExampleTiledFiles" (e.g. "C:\Program Files\Epic Games\UE_5.4\Engine\Plugins\TiledIntegration\Content\ExampleTiledFiles")

![Pick asset](https://davidonete.github.io/assets/images/tiled_integration_plugin/pick_asset.jpg)

6.- After picking the file to import you will be requested to specify the place where you want the asset to be imported to and which name you want to set. Please pick a location that is within your project content folder. You can see on the title of the window what kind of asset you want to save.

**Note:** Please pick a definitive name and location as **MOVING** or **RENAMING** the asset after it has been imported is not supported and you will need to start the process again if so.

![Pick asset](https://davidonete.github.io/assets/images/tiled_integration_plugin/save_asset.jpg)

7.- If everything went well, you should see your imported assets in the place where you specified it as well as a new dropdown option on the Control Panel from where you can manage your imported assets. From this menu you will be able to do the following:
   - **Status:** Check if the asset or the file has any issues.
   - **Asset Location:** The location of the Unreal Engine Asset.
   - **Source Location:** The location of the Tiled Asset.
   - **Auto Reimport:** If the plugin should reimport the Tiled Asset when it detects a change.
   - **Dependencies:** List of Tiled Assets that the selected asset depends on.
   - **Used By:** List of Tiled Assets that use the selected asset.
   - **Reimport:** Manually reimport the selected asset.
   - **Refresh:** Refresh the information in the Control Panel.
   - **Delete:** Delete the selected asset from Unreal Engine and it's dependencies.

![Pick asset](https://davidonete.github.io/assets/images/tiled_integration_plugin/imported_assets.jpg)

## Custom Properties
In order to support Tiled Custom Properties on Tile Maps, Tile Sets, Tiles and Layers, we have extended the default Paper2D classes to support this. We will explain how to access this classes from Blueprints and from C++ in the following sections.

### Tile Map Custom Properties
#### Blueprint
In order to access the Custom Properties of a Tile Map from blueprint you just need a reference to your Paper Tile Map Actor that is placed in your level and use the method that we provided ``Get Tile Map From Actor``. From there you can use ``Get Custom Properties`` method and get the property you want by name and type.

![Tile Map Custom Properties Blueprint](https://davidonete.github.io/assets/images/tiled_integration_plugin/tile_map_custom_properties_blueprint.jpg)

#### C++
From C++ the process is very similar. You will need a reference to the Paper Tile Map Actor and call the helper method ``GetTileMapFromActor`` from ``UTiledIntegrationTileMapLibrary`` located in ``TiledIntegrationTileMap.h`` or you can directly cast from ``UPaperTileMap`` to ``UTiledIntegrationTileMap`` and use the ``GetCustomProperties`` method to access the properties. 

If you want to use a custom class for Tile Maps you can inherit from our ``UTiledIntegrationTileMap`` class and remember to change the default class type in the Plugin Configuration (explained in a section below).

### Tile Layer Custom Properties
#### Blueprint
There are multiple options available for accessing a Tile Layer Custom Properties:
* Use the ``Get Tile Layer From Actor`` method which requires a reference to the Paper Tile Map Actor placed in your level, and use ``Get Custom Properties`` method and get the property you want by name and type.
* Use the ``Get Layer`` method from the Tiled Integration Tile Map which is returned by the ``Get Tile Map From Actor`` method explained above, and use ``Get Custom Properties`` method and get the property you want by name and type.

![Tile Layer Custom Properties Blueprint](https://davidonete.github.io/assets/images/tiled_integration_plugin/tile_layer_custom_properties_blueprint.jpg)

#### C++
There are multiple options available for accessing a Tile Layer Custom Properties:
* Use the helper method method ``GetTileLayerFromActor`` from ``UTiledIntegrationTileMapLibrary`` located in ``TiledIntegrationTileMap.h`` and then use the ``GetCustomProperties`` method to access the custom properties.
* Use the ``GetLayer`` method in ``UTiledIntegrationTileMap`` and then use the ``GetCustomProperties`` method to access the custom properties.

If you want to use a custom class for Tile Layers you can inherit from our ``UTiledIntegrationTileLayer`` class and remember to change the default class type in the Plugin Configuration (explained in a section below).
