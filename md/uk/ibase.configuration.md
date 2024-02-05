---
navigation:
  - ibase.installation.md: « Встановлення
  - ibase.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - ibase.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Конфігураційні опції InterBase**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [ibase.allow\_persistent](ibase.configuration.md#ini.ibase.allow-persistent) | "1" | **`INI_SYSTEM`** |  |
| [ibase.max\_persistent](ibase.configuration.md#ini.ibase.max-persistent) | "-1" | **`INI_SYSTEM`** |  |
| [ibase.max\_links](ibase.configuration.md#ini.ibase.max-links) | "-1" | **`INI_SYSTEM`** |  |
| [ibase.default\_db](ibase.configuration.md#ini.ibase.default-db) | NULL | **`INI_SYSTEM`** |  |
| [ibase.default\_user](ibase.configuration.md#ini.ibase.default-user) | NULL | **`INI_ALL`** |  |
| [ibase.default\_password](ibase.configuration.md#ini.ibase.default-password) | NULL | **`INI_ALL`** |  |
| [ibase.default\_charset](ibase.configuration.md#ini.ibase.default-charset) | NULL | **`INI_ALL`** |  |
| [ibase.timestampformat](ibase.configuration.md#ini.ibase.timestampformat) | "%Y-%m-%d %H:%M:%S" | **`INI_ALL`** |  |
| [ibase.dateformat](ibase.configuration.md#ini.ibase.dateformat) | "%Y-%m-%d" | **`INI_ALL`** |  |
| [ibase.timeformat](ibase.configuration.md#ini.ibase.timeformat) | "%H:%M:%S" | **`INI_ALL`** |  |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`ibase.allow_persistent`bool

Чи дозволено використовувати [постійні з'єднання](features.persistent-connections.md)к Firebird/InterBase.

`ibase.max_persistent`int

Максимальна кількість постійних з'єднань для процесу. Якщо це обмеження буде перевищено, то функція ibase\_pconnect() повертатиме непостійні з'єднання.

`ibase.max_links`int

Максимальна кількість з'єднань із Firebird/InterBase на процес, включаючи постійні.

`ibase.default_db`string

База даних за промовчанням. Якщо викликати ibase\_\[p\]connect() без вказівки імені бази даних, буде використано це значення. Якщо цей параметр встановлений і увімкнений безпечний режим SQL, будуть дозволені з'єднання тільки з цією базою.

`ibase.default_user`string

Ім'я користувача за промовчанням.

`ibase.default_password`string

Пароль за замовчуванням.

`ibase.default_charset`string

Кодування за промовчанням.

`ibase.timestampformat`string

`ibase.dateformat`string

`ibase.timeformat`string

Ці директиви використовуються для встановлення формату дати та часу. Дані формати будуть використовуватися як для отримання результуючого набору, що містить поля відповідних типів, так і при зв'язуванні значень з параметрами запиту.
