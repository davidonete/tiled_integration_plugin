---
layout: default
---

[Home](./) / Getting Started

## Getting Started
This is a quick guide of how to install and use the plugin.

[Quick Video Guide](https://www.youtube.com/watch?v=AQnpu9husAo)

**1.-** Get the plugin from the [Unreal Engine Marketplace](https://www.unrealengine.com/marketplace/en-US/product/7cde7c5f731743888f4068c8e8c24f6a) and install it into your Unreal Engine version via the Epic Games Launcher.

**2.-** Create a new project or open an existing one and activate the plugin in `Edit > Plugins > TiledIntegration`. You will have to restart Unreal Engine afterwards.

![Activate plugin](https://davidonete.github.io/tiled_integration_plugin/assets/images/tiled_integration_plugin/activate_plugin.jpg)

**3.-** After restarting Unreal Engine, you should see a new icon on the toolbar next to the play button. 

![New button](https://davidonete.github.io/tiled_integration_plugin/assets/images/tiled_integration_plugin/new_button.jpg)

**4.-** If you click it it should open the Control Panel from where you will be able to manage the Tiled Resources.

![Control Panel](https://davidonete.github.io/tiled_integration_plugin/assets/images/tiled_integration_plugin/control_panel.jpg)

**5.-** To get started simply click on the Import button at the bottom and look for a Tiled Tile Map or Tile Set file to import. 

For more details on how to import Tiled files, refer to the following guides:
  - [Import a Tile Map](./tilemaps/import.html)
  - [Import a Tile Set](./tilesets/import.html)

**6.-** If everything went well, you should see your imported assets in the place where you specified it as well as a new dropdown option on the Control Panel from where you can manage your imported assets. From this menu you will be able to do the following:
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

**7.-** If you want to quickly find a specific imported assets you can use the filter tool next to the dropdown which will let you filter by the name of the asset.