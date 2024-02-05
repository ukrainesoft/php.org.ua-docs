---
navigation:
  - odbc.installation.md: « Встановлення
  - uodbc.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - uodbc.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Установки конфігурації Unified ODBC**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [odbc.default\_db](odbc.configuration.md#ini.uodbc.default-db) \* | NULL | **`INI_ALL`** |  |
| [odbc.default\_user](odbc.configuration.md#ini.uodbc.default-user) \* | NULL | **`INI_ALL`** |  |
| [odbc.default\_pw](odbc.configuration.md#ini.uodbc.default-pw) \* | NULL | **`INI_ALL`** |  |
| [odbc.allow\_persistent](odbc.configuration.md#ini.uodbc.allow-persistent) | "1" | **`INI_SYSTEM`** |  |
| [odbc.check\_persistent](odbc.configuration.md#ini.uodbc.check-persistent) | "1" | **`INI_SYSTEM`** |  |
| [odbc.max\_persistent](odbc.configuration.md#ini.uodbc.max-persistent) | "-1" | **`INI_SYSTEM`** |  |
| [odbc.max\_links](odbc.configuration.md#ini.uodbc.max-links) | "-1" | **`INI_SYSTEM`** |  |
| [odbc.defaultlrl](odbc.configuration.md#ini.uodbc.defaultlrl) | "4096" | **`INI_ALL`** |  |
| [odbc.defaultbinmode](odbc.configuration.md#ini.uodbc.defaultbinmode) | "1" | **`INI_ALL`** |  |
| [odbc.default\_cursortype](odbc.configuration.md#ini.uodbc.defaultcursortype) | "3" | **`INI_ALL`** |  |

> **Зауваження**: Записи, позначені \*ще не реалізовані.

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`odbc.default_db`string

Джерело даних ODBC для використання, якщо жоден не вказаний у [odbc\_connect()](function.odbc-connect.md) або [odbc\_pconnect()](function.odbc-pconnect.md)

`odbc.default_user`string

Имя пользователя для использования, если ни один не указан в[odbc\_connect()](function.odbc-connect.md) або [odbc\_pconnect()](function.odbc-pconnect.md)

`odbc.default_pw`string

Пароль для использования, если ни один не указан в[odbc\_connect()](function.odbc-connect.md) або [odbc\_pconnect()](function.odbc-pconnect.md)

`odbc.allow_persistent`bool

Чи дозволяти постійні з'єднання ODBC.

`odbc.check_persistent`bool

Перед повторним використанням переконайтеся, що з'єднання все ще доступне.

`odbc.max_persistent`int

Максимальна кількість постійних з'єднань ODBC на процес.

`odbc.max_links`int

Максимальна кількість з'єднань ODBC на процес, включаючи постійні з'єднання.

`odbc.defaultlrl`int

Обробка довгих (LONG) полів. Визначає кількість байтів, що повертаються змінним. Дивіться [odbc\_longreadlen()](function.odbc-longreadlen.md) для подробиць.

Якщо вказано ціле значення (int), обсяг вимірюється байтами. Можна також використовувати скорочений запис, який описано в [у цьому розділі FAQ](faq.using.md#faq.using.shorthandbytes)

`odbc.defaultbinmode`int

Обробка двійкових даних. Дивіться [odbc\_binmode()](function.odbc-binmode.md) для подробиць.

`odbc.default_cursortype`int

Керує моделлю курсору ODBC. Можливі значення **`SQL_CURSOR_FORWARD_ONLY`** **`SQL_CURSOR_KEYSET_DRIVEN`** **`SQL_CURSOR_DYNAMIC`**и**`SQL_CURSOR_STATIC`**(по умолчанию).
