# DebugService

Сервис для управления отладочным логированием аддона.

## Подключение

[**ForgePackage**](https://github.com/Alfa-ao/ForgePackage)

```
require Alfa-ao/DebugService
```

## Использование

```lua
local config = { DEBUG = false, DEBUG_REACTION = true }

-- Создаются две функции: DebugService.LogGeneral и DebugService.LogReaction
DebugService.Init { General = config.DEBUG, Reaction = config.DEBUG_REACTION }

-- Вывод в mods.txt
DebugService.LogGeneral( 111, _G.mainForm ) -- игнорируется
DebugService.LogReaction( 222 ) -- выведет: 222


-- Дополнительно для быстроты и удобства:
log( 111, 222, {}, _G.mainForm )
```