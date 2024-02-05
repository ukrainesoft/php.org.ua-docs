---
navigation:
  - uopz.installation.md: « Встановлення
  - uopz.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - uopz.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**uopz Опції налаштування**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [uopz.disable](uopz.configuration.md#ini.uopz.disable) | "0" | **`INI_SYSTEM`** | Доступно з uopz 5.0.2 |
| [uopz.exit](uopz.configuration.md#ini.uopz.exit) | "0" | **`INI_SYSTEM`** | Доступно з uopz 6.0.1 |
| [uopz.overloads](uopz.configuration.md#ini.uopz.overloads) | "1" | **`INI_SYSTEM`** | Доступно з uopz 2.0.2. Видалено з uopz 5.0.0. |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`uopz.disable`bool

Якщо увімкнено, uopz перестане впливати на роботу PHP.

`uopz.exit`bool

Чи дозволяти модулю виконувати опкод exit (вихід). Ця установка може бути перевизначена під час виконання за допомогою функції [uopz\_allow\_exit()](function.uopz-allow-exit.md)

`uopz.overloads`bool

Дає можливість використовувати [uopz\_overload()](function.uopz-overload.md)

> **Зауваження**: Під час роботи з увімкненим OPcache може знадобитися вимкнути все [оптимізації OPcache](opcache.configuration.md#ini.opcache.optimization-level) `opcache.optimization_level=0`
