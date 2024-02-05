---
navigation:
  - pgsql.installation.md: « Встановлення
  - pgsql.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - pgsql.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Параметри конфігурації PostgreSQL**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [pgsql.allow\_persistent](pgsql.configuration.md#ini.pgsql.allow-persistent) | "1" | **`INI_SYSTEM`** |  |
| [pgsql.max\_persistent](pgsql.configuration.md#ini.pgsql.max-persistent) | "-1" | **`INI_SYSTEM`** |  |
| [pgsql.max\_links](pgsql.configuration.md#ini.pgsql.max-links) | "-1" | **`INI_SYSTEM`** |  |
| [pgsql.auto\_reset\_persistent](pgsql.configuration.md#ini.pgsql.auto-reset-persistent) | "0" | **`INI_SYSTEM`** |  |
| [pgsql.ignore\_notice](pgsql.configuration.md#ini.pgsql.ignore-notice) | "0" | **`INI_ALL`** |  |
| [pgsql.log\_notice](pgsql.configuration.md#ini.pgsql.log-notice) | "0" | **`INI_ALL`** |  |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`pgsql.allow_persistent`bool

Чи слід дозволити постійне з'єднання з Postgres.

`pgsql.max_persistent`int

Максимальна кількість постійних з'єднань на один процес.

`pgsql.max_links`int

Максимальна кількість з'єднань Postgres на процес, включаючи постійні з'єднання.

`pgsql.auto_reset_persistent`int

Визначати розірвані постійні посилання з [pg\_pconnect()](function.pg-pconnect.md). Потрібні невеликі ресурси.

`pgsql.ignore_notice`int

Ігнорувати чи ні повідомлення від PostgreSQL.

`pgsql.log_notice`int

Чи записувати в лог повідомлення від PostgreSQL. Для запису в лог повідомлення також необхідно вимкнути PHP-директиву [pgsql.ignore\_notice](pgsql.configuration.md#ini.pgsql.ignore-notice)
