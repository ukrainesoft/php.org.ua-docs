---
navigation:
  - function.dba-popen.html: « dbapopen
  - function.dba-sync.html: dbasync »
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

Обробник бази даних, повернутий [dbaopen()](function.dba-open.html) або [dbapopen()](function.dba-popen.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [dbaexists()](function.dba-exists.html) - Перевіряє, чи існує ключ
-   [dbadelete()](function.dba-delete.html) - Видаляє запис бази даних, визначену ключем
-   [dbafetch()](function.dba-fetch.html) - Витягує дані за вказаним ключем
-   [dbainsert()](function.dba-insert.html) - Вставляє запис
