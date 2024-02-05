---
navigation:
  - function.ibase-free-query.md: « ibase\_free\_query
  - function.ibase-gen-id.md: ibase\_gen\_id »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_free\_result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_free\_result

(PHP 5, PHP 7 < 7.4.0)

ibase\_free\_result — Звільняє набір результатів

### Опис

```methodsynopsis
ibase_free_result(resource $result_identifier): bool
```

Звільняє набір результатів.

### Список параметрів

`result_identifier`

Набір результатів, створених за допомогою [ibase\_query()](function.ibase-query.md) або [ibase\_execute()](function.ibase-execute.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
