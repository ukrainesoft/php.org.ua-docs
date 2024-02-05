---
navigation:
  - function.dba-delete.md: « dba\_delete
  - function.dba-fetch.md: dba\_fetch »
  - index.md: PHP Manual
  - ref.dba.md: Функції DBA
title: dba\_exists
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dba\_exists

(PHP 4, PHP 5, PHP 7, PHP 8)

dba\_exists — Перевіряє, чи існує ключ

### Опис

```methodsynopsis
dba_exists(string|array $key, resource $dba): bool
```

**dba\_exists()** перевіряє, якщо у базі даних заданий ключ `key`

### Список параметрів

`key`

Ключ, що перевіряється.

`dba`

Обробник бази даних, повернутий [dba\_open()](function.dba-open.md) або [dba\_popen()](function.dba-popen.md)

### Значення, що повертаються

Повертає **`true`** якщо ключ існує і \*\*`false`\*\*в обратном случае.

### Дивіться також

-   [dba\_delete()](function.dba-delete.md) \- Видаляє запис бази даних, визначену ключем
-   [dba\_fetch()](function.dba-fetch.md) \- Витягує дані за вказаним ключем
-   [dba\_insert()](function.dba-insert.md) \- Вставляє запис
-   [dba\_replace()](function.dba-replace.md) \- Перезаписати або вставити запис
