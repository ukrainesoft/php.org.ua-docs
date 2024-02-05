---
navigation:
  - yar.installation.md: « Встановлення
  - yar.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - yar.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Yar Опції налаштування**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [yar.packager](yar.configuration.md#ini.yar.packager) | php | **`INI_SYSTEM`** |  |
| [yar.debug](yar.configuration.md#ini.yar.debug) | Off | **`INI_ALL`** |  |
| [yar.connect\_timeout](yar.configuration.md#ini.yar.connect-timeout) | 1000 | **`INI_ALL`** |  |
| [yar.timeout](yar.configuration.md#ini.yar.timeout) | 5000 | **`INI_ALL`** |  |
| [yar.expose\_info](yar.configuration.md#ini.yar.expose-info) | On | **`INI_SYSTEM`** |  |

Коротке пояснення конфігураційних директив.

`yar.packager`string

може бути php, json та msgpack (потрібна вбудована підтримка msgpack)

`yar.debug`string

`yar.connect_timeout`int

Час очікування з'єднання у мілісекундах.

`yar.timeout`int

Час очікування у мілісекундах.

`yar.expose_info`bool

чи розкривати дані сервера (при доступі за допомогою GET)
