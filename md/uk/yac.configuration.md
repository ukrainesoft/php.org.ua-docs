---
navigation:
  - yac.installation.md: « Встановлення
  - yac.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - yac.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Yac**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [yac.compress\_threshold](yac.configuration.md#ini.yac.compress-threshold) | \- | **`INI_SYSTEM`** |  |
| [yac.debug](yac.configuration.md#ini.yac.debug) |  | **`INI_ALL`** |  |
| [yac.enable](yac.configuration.md#ini.yac.enable) |  | **`INI_SYSTEM`** |  |
| [yac.enable\_cli](yac.configuration.md#ini.yac.enable-cli) |  | **`INI_SYSTEM`** |  |
| [yac.keys\_memory\_size](yac.configuration.md#ini.yac.keys-memory-size) | 4M | **`INI_SYSTEM`** |  |
| [yac.serializer](yac.configuration.md#ini.yac.serializer) | php | **`INI_SYSTEM`** |  |
| [yac.values\_memory\_size](yac.configuration.md#ini.yac.values-memory-size) | 64M | **`INI_SYSTEM`** |  |

Коротке пояснення конфігураційних директив.

`yac.compress_threshold`int

`yac.debug`int

`yac.enable`int

`yac.enable_cli`int

`yac.keys_memory_size`string

`yac.serializer`string

`yac.values_memory_size`string
