---
navigation:
  - sqlite3.installation.md: « Встановлення
  - sqlite3.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - sqlite3.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування SQLite3**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [sqlite3.extension\_dir](sqlite3.configuration.md#ini.sqlite3.extension-dir) | "" | **`INI_SYSTEM`** |  |
| [sqlite3.defensive](sqlite3.configuration.md#ini.sqlite3.defensive) |  | **`INI_USER`** | Доступно, починаючи з PHP 7.2.17 та 7.3.4 для libsqlite ≥ 3.26.0. До PHP 8.2.0 цей параметр можна було змінити лише як **`INI_SYSTEM`** |

Коротке пояснення конфігураційних директив.

`sqlite3.extension_dir`string

Шлях до каталогу, де знаходяться файли модуля SQLite.

`sqlite3.defensive`bool

Якщо встановлено прапор defensive, мовні конструкції, які дозволяють звичайному SQL-запиту навмисно ушкоджувати файл бази даних, вимкнено. Забороняється запис безпосередньо у схему, в тіньові таблиці (тобто таблиці даних FTS) або віртуальну таблицю sqlite\_dbpage. Це налаштування php.ini працює лише з libsqlite ≥ 3.26.0.
