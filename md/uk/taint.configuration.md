---
navigation:
  - taint.installation.md: « Встановлення
  - taint.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - taint.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Taint**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [taint.enable](taint.configuration.md#ini.taint.enable) |  | **`INI_SYSTEM`** |  |
| [taint.error\_level](taint.configuration.md#ini.taint.error-level) | E\_WARNING | **`INI_ALL`** |  |

Коротке пояснення конфігураційних директив.

`taint.enable`int

Чи включений модуль.

`taint.error_level`int

Тип помилки, який повертатиме модуль при виявленні підозрілого рядка.
