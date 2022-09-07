---
navigation:
  - phpdbg.setup.md: « Встановлення та налаштування
  - phpdbg.constants.md: Обумовлені константи »
  - index.md: PHP Manual
  - phpdbg.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**phpdbg Опції налаштування**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [phpdbg.eol](phpdbg.configuration.md#ini.phpdbg.eol) |  | PHPINIALL | Видалено, починаючи з PHP 8.1.0 |
| [phpdbg.path](phpdbg.configuration.md#ini.phpdbg.path) |  |  | Видалено, починаючи з PHP 8.1.0 |

Коротке пояснення конфігураційних директив.

`phpdbg.eol` [mixed](language.types.declarations.md#language.types.declarations.mixed)

Тип закінчення рядка, який використовується для виведення. Для встановлення значення необхідно використовувати один із псевдонімів рядків.

| int Значение | string Псевдоним |
| --- | --- |
| `0` | `CRLF` `crlf` `DOS` `dos` |
| `1` | `LF` `lf` `UNIX` `unix` |
| `2` | `CR` `cr` `MAC` `mac` |

`phpdbg.path` string
