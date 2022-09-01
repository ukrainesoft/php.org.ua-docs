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

Обробник бази даних, повернутий [dbaopen()](function.dba-open.html) або [dbapopen()](function.dba-popen.html)

### Значення, що повертаються

Повертає **`true`** якщо ключ існує і **`false`** в зворотньому випадку.

### Дивіться також

-   [dbadelete()](function.dba-delete.html) - Видаляє запис бази даних, визначену ключем
-   [dbafetch()](function.dba-fetch.html) - Витягує дані за вказаним ключем
-   [dbainsert()](function.dba-insert.html) - Вставляє запис
-   [dbareplace()](function.dba-replace.html) - Перезаписати або вставити запис
