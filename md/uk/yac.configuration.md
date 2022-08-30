Налаштування під час виконання

-   [« Установка](yac.installation.md)
    
-   [Типи ресурсів »](yac.resources.md)
    
-   [PHP Manual](index.md)
    
-   [Встановлення та налаштування](yac.setup.md)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Yac**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [yac.compressthreshold](yac.configuration.html#ini.yac.compress-threshold) |  | PHPINISYSTEM |  |
| [yac.debug](yac.configuration.html#ini.yac.debug) |  | PHPINIALL |  |
| [yac.enable](yac.configuration.html#ini.yac.enable) |  | PHPINISYSTEM |  |
| [yac.enablecli](yac.configuration.html#ini.yac.enable-cli) |  | PHPINISYSTEM |  |
| [yac.keysmemorysize](yac.configuration.html#ini.yac.keys-memory-size) | ЧС | PHPINISYSTEM |  |
| [yac.serializer](yac.configuration.html#ini.yac.serializer) | php | PHPINISYSTEM |  |
| [yac.valuesmemorysize](yac.configuration.html#ini.yac.values-memory-size) | 64M | PHPINISYSTEM |  |

Коротке пояснення конфігураційних директив.

`yac.compress_threshold` int

`yac.debug` int

`yac.enable` int

`yac.enable_cli` int

`yac.keys_memory_size` string

`yac.serializer` string

`yac.values_memory_size` string