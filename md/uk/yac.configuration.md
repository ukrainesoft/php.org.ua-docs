---
navigation:
  - yac.installation.md: « Установка
  - yac.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - yac.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Yac**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [yac.compressthreshold](yac.configuration.md#ini.yac.compress-threshold) |  | PHPINISYSTEM |  |
| [yac.debug](yac.configuration.md#ini.yac.debug) |  | PHPINIALL |  |
| [yac.enable](yac.configuration.md#ini.yac.enable) |  | PHPINISYSTEM |  |
| [yac.enablecli](yac.configuration.md#ini.yac.enable-cli) |  | PHPINISYSTEM |  |
| [yac.keysmemorysize](yac.configuration.md#ini.yac.keys-memory-size) | ЧС | PHPINISYSTEM |  |
| [yac.serializer](yac.configuration.md#ini.yac.serializer) | php | PHPINISYSTEM |  |
| [yac.valuesmemorysize](yac.configuration.md#ini.yac.values-memory-size) | 64M | PHPINISYSTEM |  |

Коротке пояснення конфігураційних директив.

`yac.compress_threshold` int

`yac.debug` int

`yac.enable` int

`yac.enable_cli` int

`yac.keys_memory_size` string

`yac.serializer` string

`yac.values_memory_size` string
