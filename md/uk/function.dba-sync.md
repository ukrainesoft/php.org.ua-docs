---
navigation:
  - function.dba-replace.md: « dbareplace
  - book.uodbc.md: ODBC »
  - index.md: PHP Manual
  - ref.dba.md: Функції DBA
title: dbasync
---
# dbasync

(PHP 4, PHP 5, PHP 7, PHP 8)

dbasync — Синхронізує базу даних

### Опис

```methodsynopsis
dba_sync(resource $dba): bool
```

**dbasync()** синхронізує базу даних. Швидше за все, якщо підтримується ця функція, викличе запис на диск.

### Список параметрів

`dba`

Обробник бази даних, повернутий [dbaopen()](function.dba-open.md) або [dbapopen()](function.dba-popen.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [dbaoptimize()](function.dba-optimize.md) - Оптимізує базу даних
