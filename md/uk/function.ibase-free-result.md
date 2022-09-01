---
navigation:
  - function.ibase-free-query.html: « ibasefreequery
  - function.ibase-gen-id.html: ibasegenid »
  - index.html: PHP Manual
  - ref.ibase.html: Функции Firebird/InterBase
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

Набір результатів, створених за допомогою [ibasequery()](function.ibase-query.html) або [ibaseexecute()](function.ibase-execute.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
