---
navigation:
  - igbinary.installation.md: « Установка
  - ref.igbinary.md: Функции Igbinary »
  - index.md: PHP Manual
  - igbinary.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Igbinary**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [igbinary.compactstrings](igbinary.configuration.md#ini.igbinary.compact-strings) |  | PHPINIALL |  |

**Параметри конфігурації сесії, що впливають на поведінку Igbinary**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [session.savehandler](igbinary.configuration.md#ini.igbinary.save-handler) | "files" | PHPINIALL |  |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Коротке пояснення конфігураційних директив.

`igbinary.compact_strings` bool

Увімкнення або вимкнення стиснення рядків, що повторюються. За промовчанням On (увімкнено).

`session.save_handler` string

Igbinary буде використовуватися як обробник сесії, якщо встановити значення `igbinary`
