---
navigation:
  - function.dba-popen.md: « dbapopen
  - function.dba-sync.md: dbasync »
  - index.md: PHP Manual
  - ref.dba.md: Функції DBA
title: dbareplace
---
# dbareplace

(PHP 4, PHP 5, PHP 7, PHP 8)

dbareplace — Перезаписати або вставити запис

### Опис

```methodsynopsis
dba_replace(string|array $key, string $value, resource $dba): bool
```

**dbareplace()** перезаписує або вставляє запис, заданий ключем `key` та значенням `value` до бази даних, визначеної обробником `dba`

### Список параметрів

`key`

Ключ запису, який потрібно замінити.

`value`

Нове значення.

`dba`

Обробник бази даних, повернутий [dbaopen()](function.dba-open.md) або [dbapopen()](function.dba-popen.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [dbaexists()](function.dba-exists.md) - Перевіряє, чи існує ключ
-   [dbadelete()](function.dba-delete.md) - Видаляє запис бази даних, визначену ключем
-   [dbafetch()](function.dba-fetch.md) - Витягує дані за вказаним ключем
-   [dbainsert()](function.dba-insert.md) - Вставляє запис
