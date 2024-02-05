---
navigation:
  - function.ibase-free-event-handler.md: « ibase\_free\_event\_handler
  - function.ibase-free-result.md: ibase\_free\_result »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_free\_query
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_free\_query

(PHP 5, PHP 7 < 7.4.0)

ibase\_free\_query — Звільняє пам'ять, виділену для підготовки запиту

### Опис

```methodsynopsis
ibase_free_query(resource $query): bool
```

Визволяє підготовлений запит.

### Список параметрів

`query`

Запит, підготовлений за допомогою [ibase\_prepare()](function.ibase-prepare.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
