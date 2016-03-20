# Secure Safezones For ExileMod - [Download](https://github.com/Gr8z/ExileMod-SecureSafezones/archive/master.zip)
This script is made to ensure your full safety in a safezone by stopping other people to steal your vehicle and/or its contents. Fully customizable and easy to install, this should hopefully remove the big hassle of having an admin punishing safezone theifs all the time and make this process automated.

All these features below you can enable/disable :

- Kicks out all players outside your group from your vehicle.
- Players outside your group won't be able to check the gear.
- Players outside your group won't be able to sell your vehicle.
- Get in the driver's seat to claim ownership.

### Install Intructions ###

- Add this at the end of your **initPlayerLocal.sqf** in your missions PBO.
```
// Secure Safezones by Gr8
[] execVM "SecureSafezones\config.sqf";
```

- Copy the **SecureSafezones** folder in your Mission PBO.

- Open **config.cpp** in your mission file.
- Look for:
```
class CfgExileCustomCode
{
```
- Add this Below:
```
ExileClient_object_player_thread_safeZone = 			"SecureSafezones\GG_safeZone.sqf";
ExileClient_object_player_event_onEnterSafezone = 		"SecureSafezones\GG_onEnterSafezone.sqf";
ExileClient_object_player_event_onLeaveSafezone = 		"SecureSafezones\GG_onLeaveSafezone.sqf";
ExileServer_system_trading_network_wasteDumpRequest = 	"SecureSafezones\GG_wasteDumpRequest.sqf";
```


### BattlEye Filters ###

setVariable.txt
scripts.txt

### BattlEye Filters ###

Thank you [†RiH† StokesMagee](http://www.exilemod.com/profile/52663-%E2%80%A0rih%E2%80%A0-stokesmagee/) for helping and testing this script.