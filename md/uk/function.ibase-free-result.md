---
navigation:
  - function.ibase-free-query.md: « ibasefreequery
  - function.ibase-gen-id.md: ibasegenid »
  - index.md: PHP Manual
  - ref.ibase.md: Функции Firebird/InterBase
title: ibasefreeresult
---
# ibasefreeresult

(PHP 5, PHP 7 < 7.4.0)

ibasefreeresult — Звільняє набір результатів

### Опис

```methodsynopsis
ibase_free_result(resource $result_identifier): bool
```

Звільняє набір результатів.

### Список параметрів

`result_identifier`

Набір результатів, створених за допомогою [ibasequery()](function.ibase-query.md) або [ibaseexecute()](function.ibase-execute.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
