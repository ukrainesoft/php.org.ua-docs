---
navigation:
  - yaconf.installation.md: « Установка
  - yaconf.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - yaconf.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Yaconf**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [yaconf.checkdelay](yaconf.configuration.html#ini.yaconf.check-delay) |  | PHPINISYSTEM |  |
| [yaconf.directory](yaconf.configuration.html#ini.yaconf.directory) | /tmp/conf/ | PHPINISYSTEM |  |

Коротке пояснення конфігураційних директив.

`yaconf.check_delay` int

Інтервал часу, протягом якого Yaconf визначатиме зміну файлу ini (за часом зміни директорії), якщо встановлено нуль, потрібно перезапуск PHP для перезавантаження конфігурацій.

`yaconf.directory` string

Шлях до директорії, де знаходяться всі файли конфігурації INI.
