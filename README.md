# SanJuanProjet

Central economy files for a San Juan Project server

## Setup

Simply put this folder into your server missions folder and load it like any other mission file.
This works for both online and offline just make sure to copy over the files needed for COT.

### Adding custom buildings and areas

If you add custom locations/buildings to the map and want loot to spawn on these new locations you need to do as follows.

In the mission files init.c you want to find the lines:

```
	//INIT ECONOMY--------------------------------------
	Hive ce = CreateHive();
	if ( ce )
		ce.InitOffline();
	
	//GetCEApi().ExportProxyData( "10240 0 10240", 20480 );  //Center of map, radius of how far to go out and find buildings.
```
Now remove the two // infront of the line ```GetCEApi().ExportProxyData( "10240 0 10240", 20480 );  //Center of map, radius of how far to go out and find buildings.```

## Authors

* **Jake Tommas** - *Map Creator* - [Jake Tommas](https://steamcommunity.com/id/lifes_a_bitch_get_over_it/)
