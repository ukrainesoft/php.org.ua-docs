---
navigation:
  - geoip.installation.md: « Встановлення
  - geoip.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - geoip.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції настроювання GeoIP**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [geoip.custom\_directory](geoip.configuration.md#ini.geoip.custom-directory) | "" | **`INI_ALL`** |  |

Коротке пояснення конфігураційних директив.

`geoip.custom_directory`string

За замовчуванням порожня, але може бути встановлена ​​для примусового використання іншого шляху до бази даних, ніж зазначеної у бібліотеці.
