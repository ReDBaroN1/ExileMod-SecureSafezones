# Secure Safezones For ExileMod - [Download](https://github.com/Gr8z/ExileMod-SecureSafezones/archive/master.zip)
Данный скрипт сделан для полной вашей безопасности в safezone, не давая другим игрокам украсть Ваш автомобиль  либо его содержимое. Полностью настраиваемый и простой в установке .

Все эти функции ниже вы можете вкл/отк :

- Выкидывает всех игроков из транспорта, если они не в вашей группе.
- Игроков не из вашей группы не сможет проверить инвентарь.
- Игроков не из вашей группы не сможет продать ваш транспорт.


### Установка ###

- Добавьте это в конец вашего **initPlayerLocal.sqf** в вашей миссии PBO.
```
// Secure Safezones by Gr8
[] execVM "SecureSafezones\config.sqf";
```

- Скопировать **SecureSafezones** в папку в вашей миссии PBO.

- Открыть **config.cpp** в файле миссии.
- Искать:
```
class CfgExileCustomCode
{
```
- Добавить:
```
ExileClient_object_player_thread_safeZone = 			"SecureSafezones\GG_safeZone.sqf";
ExileClient_object_player_event_onEnterSafezone = 		"SecureSafezones\GG_onEnterSafezone.sqf";
ExileClient_object_player_event_onLeaveSafezone = 		"SecureSafezones\GG_onLeaveSafezone.sqf";
ExileServer_system_trading_network_wasteDumpRequest = 	"SecureSafezones\GG_wasteDumpRequest.sqf";
ExileClient_object_player_event_onInventoryOpened = 	"SecureSafezones\GG_onInventoryOpened.sqf";
```


### BattlEye Фильтры ###

- setVariable.txt
- scripts.txt

### Credits ###

Спасибо [†RiH† StokesMagee](http://www.exilemod.com/profile/52663-%E2%80%A0rih%E2%80%A0-stokesmagee/) за помощь и тестирование этого сценария.
