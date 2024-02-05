---
navigation:
  - function.dba-open.md: « dba\_open
  - function.dba-popen.md: dba\_popen »
  - index.md: PHP Manual
  - ref.dba.md: Функції DBA
title: dba\_optimize
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dba\_optimize

(PHP 4, PHP 5, PHP 7, PHP 8)

dba\_optimize - Оптимізує базу даних

### Опис

```methodsynopsis
dba_optimize(resource $dba): bool
```

**dba\_optimize()** оптимізує основну базу даних

### Список параметрів

`dba`

Обробник бази даних, повернутий [dba\_open()](function.dba-open.md) або [dba\_popen()](function.dba-popen.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [dba\_sync()](function.dba-sync.md) \- Синхронізує базу даних
