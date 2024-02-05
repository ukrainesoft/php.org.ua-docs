---
navigation:
  - mysql-xdevapi.installation.md: « Встановлення
  - mysql-xdevapi.build.md: Складання / Компіляція з вихідного коду »
  - index.md: PHP Manual
  - mysql-xdevapi.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Mysql\_xdevapi**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [xmysqlnd.collect\_memory\_statistics](mysql-xdevapi.configuration.md#ini.xmysqlnd.collect-memory-statistics) |  | **`INI_SYSTEM`** |  |
| [xmysqlnd.collect\_statistics](mysql-xdevapi.configuration.md#ini.xmysqlnd.collect-statistics) |  | **`INI_ALL`** |  |
| [xmysqlnd.debug](mysql-xdevapi.configuration.md#ini.xmysqlnd.debug) |  | **`INI_SYSTEM`** |  |
| [xmysqlnd.mempool\_default\_size](mysql-xdevapi.configuration.md#ini.xmysqlnd.mempool-default-size) | 16000 | **`INI_ALL`** |  |
| [xmysqlnd.net\_read\_timeout](mysql-xdevapi.configuration.md#ini.xmysqlnd.net-read-timeout) | 31536000 | **`INI_SYSTEM`** |  |
| [xmysqlnd.trace\_alloc](mysql-xdevapi.configuration.md#ini.xmysqlnd.trace-alloc) |  | **`INI_SYSTEM`** |  |

Коротке пояснення конфігураційних директив.

`xmysqlnd.collect_memory_statistics`int

`xmysqlnd.collect_statistics`int

`xmysqlnd.debug`string

`xmysqlnd.mempool_default_size`int

`xmysqlnd.net_read_timeout`int

`xmysqlnd.trace_alloc`string
