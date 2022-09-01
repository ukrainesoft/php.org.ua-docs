---
navigation:
  - taint.installation.md: « Установка
  - taint.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - taint.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Taint**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [taint.enable](taint.configuration.html#ini.taint.enable) |  | PHPINISYSTEM |  |
| [taint.errorlevel](taint.configuration.html#ini.taint.error-level) | ЕWARNING | PHPINIALL |  |

Коротке пояснення конфігураційних директив.

`taint.enable` int

Чи увімкнено модуль.

`taint.error_level` int

Тип помилки, який повертатиме модуль при виявленні підозрілого рядка.
