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

## Advanced
