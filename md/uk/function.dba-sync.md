---
navigation:
  - function.dba-replace.md: « dba\_replace
  - book.uodbc.md: ODBC »
  - index.md: PHP Manual
  - ref.dba.md: Функції DBA
title: dba\_sync
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dba\_sync

(PHP 4, PHP 5, PHP 7, PHP 8)

dba\_sync — Синхронізує базу даних

### Опис

```methodsynopsis
dba_sync(resource $dba): bool
```

**dba\_sync()** синхронізує базу даних. Швидше за все, якщо підтримується ця функція, викличе запис на диск.

### Список параметрів

`dba`

Обробник бази даних, повернутий [dba\_open()](function.dba-open.md) або [dba\_popen()](function.dba-popen.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [dba\_optimize()](function.dba-optimize.md) \- Оптимізує базу даних
