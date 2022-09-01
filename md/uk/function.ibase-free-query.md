---
navigation:
  - function.ibase-free-event-handler.html: « ibasefreeeventhandler
  - function.ibase-free-result.html: ibasefreeresult »
  - index.md: PHP Manual
  - ref.ibase.md: Функции Firebird/InterBase
title: ibasefreequery
---
# ibasefreequery

(PHP 5, PHP 7 < 7.4.0)

ibasefreequery — Звільняє пам'ять, виділену для підготовки запиту

### Опис

```methodsynopsis
ibase_free_query(resource $query): bool
```

Звільняє підготовлений запит.

### Список параметрів

`query`

Запит, підготовлений за допомогою [ibaseprepare()](function.ibase-prepare.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
