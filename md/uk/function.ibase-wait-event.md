---
navigation:
  - function.ibase-trans.html: « ibasetrans
  - book.ibm-db2.html: IBM DB2 »
  - index.md: PHP Manual
  - ref.ibase.md: Функции Firebird/InterBase
title: ibasewaitevent
---
# ibasewaitevent

(PHP 5, PHP 7 < 7.4.0)

ibasewaitevent — Чекаємо, доки подія буде опублікована в базі даних

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

-   [ibaseseteventhandler()](function.ibase-set-event-handler.html) - Реєструє callback-функцію, яка буде викликатись при публікації подій
-   [ibasefreeeventhandler()](function.ibase-free-event-handler.html) - скасовує зареєстрований обробник події
