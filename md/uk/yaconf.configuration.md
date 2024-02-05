---
navigation:
  - yaconf.installation.md: « Встановлення
  - yaconf.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - yaconf.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Yaconf**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [yaconf.check\_delay](yaconf.configuration.md#ini.yaconf.check-delay) | 300 | **`INI_SYSTEM`** |  |
| [yaconf.directory](yaconf.configuration.md#ini.yaconf.directory) | /tmp/conf/ | **`INI_SYSTEM`** |  |

Коротке пояснення конфігураційних директив.

`yaconf.check_delay`int

Інтервал часу, протягом якого Yaconf визначатиме зміну файлу ini (за часом зміни директорії), якщо встановлено нуль, потрібно перезапуск PHP для перезавантаження конфігурацій.

`yaconf.directory`string

Шлях до директорії, де знаходяться всі файли конфігурації INI.
