---
navigation:
  - function.ibase-field-info.md: « ibase\_field\_info
  - function.ibase-free-query.md: ibase\_free\_query »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_free\_event\_handler
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_free\_event\_handler

(PHP 5, PHP 7 < 7.4.0)

ibase\_free\_event\_handler — скасовує зареєстрований обробник події

### Опис

```methodsynopsis
ibase_free_event_handler(resource $event): bool
```

Функція скасовує, зареєстрований обробник події, зазначений у `event`. Callback-функція більше не буде викликатись для подій, для яких вона була зареєстрована.

### Список параметрів

`event`

Ресурс події, створений [ibase\_set\_event\_handler()](function.ibase-set-event-handler.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ibase\_set\_event\_handler()](function.ibase-set-event-handler.md) \- Реєструє callback-функцію, яка буде викликатись при публікації подій
