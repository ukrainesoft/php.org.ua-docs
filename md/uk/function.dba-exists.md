---
navigation:
  - function.dba-delete.html: « dbadelete
  - function.dba-fetch.html: dbafetch »
  - index.md: PHP Manual
  - ref.dba.md: Функції DBA
title: dbaexists
---
# dbaexists

(PHP 4, PHP 5, PHP 7, PHP 8)

dbaexists — Перевіряє, чи існує ключ

### Опис

```methodsynopsis
dba_exists(string|array $key, resource $dba): bool
```

**dbaexists()** перевіряє, якщо у базі даних заданий ключ `key`

### Список параметрів

`key`

Ключ, що перевіряється.

`dba`

Обробник бази даних, повернутий [dbaopen()](function.dba-open.html) або [dbapopen()](function.dba-popen.md)

### Значення, що повертаються

Повертає **`true`** якщо ключ існує і **`false`** в зворотньому випадку.

### Дивіться також

-   [dbadelete()](function.dba-delete.md) - Видаляє запис бази даних, визначену ключем
-   [dbafetch()](function.dba-fetch.md) - Витягує дані за вказаним ключем
-   [dbainsert()](function.dba-insert.md) - Вставляє запис
-   [dbareplace()](function.dba-replace.md) - Перезаписати або вставити запис
