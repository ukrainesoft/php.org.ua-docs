---
navigation:
  - function.ibase-trans.md: « ibase\_trans
  - book.ibm-db2.md: IBM DB2 »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_wait\_event
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_wait\_event

(PHP 5, PHP 7 < 7.4.0)

ibase\_wait\_event — Чекаємо, доки подія буде опублікована в базі даних

### Опис

```methodsynopsis
ibase_wait_event(string $event_name, string ...$event_names): string
```

```methodsynopsis
ibase_wait_event(resource $connection, string $event_name, string ...$event_names): string
```

Функція призупиняє виконання сценарію до тих пір, поки одна з зазначених подій не буде опублікована в базі даних. Ім'я події, яку було опубліковано, повертається. Функція ухвалює до 15 аргументів події.

### Список параметрів

`event_name`

Назва події.

`event_names`

### Значення, що повертаються

Повертає назву події, яка була опублікована.

### Дивіться також

-   [ibase\_set\_event\_handler()](function.ibase-set-event-handler.md) \- Реєструє callback-функцію, яка буде викликатись при публікації подій
-   [ibase\_free\_event\_handler()](function.ibase-free-event-handler.md) \- скасовує зареєстрований обробник події
