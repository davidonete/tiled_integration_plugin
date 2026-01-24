---
layout: default
---

[Home](../) / [Tiles](./index.md) / Tile Actor Spawner

## Tile Actor Spawner
The tile actor spawner is a feature in this plugin to allow spawning any kind of UE Actor in a specified tile. This will happen whenever a [Tile Map Actor](../tilemaps/atilemapactor.html) or a [Tile World Actor](../worlds/atileworldactor.html) is added into a level while having one or more Tiles configured to spawn the actors.

**1.-** In Tiled, open the Tile Set that contains the desired tile that will be used to spawn a UE Actor.

**Note:** I would recommend creating a "Spawner" Tile Set where you have all the tiles that spawn UE Actors in one place.

**2.-** Select the desired Tile and you can either:

- Add ```ActorSpawnerID``` as a string, ```ActorSpawnerOffsetX``` as a float, ```ActorSpawnerOffsetY``` as a float and ```ActorSpawnerOffsetZ``` as a float, for the custom properties of the desired tile.

- If you have the predefined [Custom Properties](./custom-properties.html), you can set the class to ```Tile``` and you will see all the available custom properties.

**3.-** In the ```ActorSpawnerID``` custom property you will have to specify a unique string ID that will be used to pair this tile with the actor to spawn in UE.

**4.-** In the ```ActorSpawnerOffsetX```, ```ActorSpawnerOffsetY``` and ```ActorSpawnerOffsetZ```, you can specify an optional offset from the center of the tile that will be used to spawn the UE Actor.

**5.-** Once all your changes are done, save the Tile Set and place the new tiles in any of your Tile Maps and save it.

**6.-** In UE, go to ```Project Settings``` > ```Tiled Integration``` > ```Tile Actor Spawner```. In there you can add as many tile actor spawners as you wish just by clicking on the "+" button to add a new element and specifying the ID as the unique ID you set on step 3 and then a reference to the actor blueprint you would like to spawn.

**Note:** The IDs have to be unique between all the Tile Actor Spawners created.

**7.-** Finally, import/reimport the Tile Set modified in step 1 as well as the Tile Map modified in step 5. If your Tile Map was already in a level, you should see the new actors being spawned, if not, they will spawn when you add the Tile Map or Tile World into the level.