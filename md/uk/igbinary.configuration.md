---
navigation:
  - igbinary.installation.md: « Встановлення
  - ref.igbinary.md: Функції Igbinary »
  - index.md: PHP Manual
  - igbinary.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Igbinary**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [igbinary.compact\_strings](igbinary.configuration.md#ini.igbinary.compact-strings) |  | **`INI_ALL`** |  |

**Параметри конфігурації сесії, що впливають на поведінку Igbinary**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [session.save\_handler](igbinary.configuration.md#ini.igbinary.save-handler) | "files" | **`INI_ALL`** |  |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`igbinary.compact_strings`bool

Увімкнення або вимкнення стиснення рядків, що повторюються. За промовчанням On (увімкнено).

`session.save_handler`string

Igbinary буде використовуватися як обробник сесії, якщо встановити значення `igbinary`
