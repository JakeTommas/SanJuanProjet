# SanJuanProjet

Pre-configured mission file for the SanJuanProject Map with CE and custom spawnpoints for players, animals and zombies.

## Setup

Simply put this folder into your server missions folder and load it like any other mission file.
This works for both online and offline just make sure to copy over the files needed for COT.

### Adding custom buildings and areas

If you add custom locations/buildings to the map and want loot to spawn on these new locations you need to do as follows.

In the mission files ```init.c``` you want to find the lines:

```	//INIT ECONOMY--------------------------------------
	Hive ce = CreateHive();
	if ( ce )
		ce.InitOffline();
	
	//GetCEApi().ExportProxyData( "10240 0 10240", 20480 );  //Center of map, radius of how far to go out and find buildings.
```
Now remove the two ```//``` infront of the line ```GetCEApi().ExportProxyData( "10240 0 10240", 20480 );  //Center of map, radius of how far to go out and find buildings.```.
Load into the server and login as the server admin as followed ```#login "adminpassword``` Then type ```#shutdown``` and wait for the server to shutdown.
Reopen the ```init.c``` and readd in the two ```//```.
Load the server and you will be good to go.

## Author

* **Jake Tommas** - *Map Creator* - [Jake Tommas](https://steamcommunity.com/id/lifes_a_bitch_get_over_it/)

## Contributors

* Zeroy - *Helping with custom surface setup*
* Arkensor - *Being an all round Dayz Modding God*
* Anyone else from the Dayz Modders [discord](https://discord.gg/eMhjTWS)
