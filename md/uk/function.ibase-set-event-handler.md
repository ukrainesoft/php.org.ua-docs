---
navigation:
  - function.ibase-service-detach.md: « ibase\_service\_detach
  - function.ibase-trans.md: ibase\_trans »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_set\_event\_handler
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_set\_event\_handler

(PHP 5, PHP 7 < 7.4.0)

ibase\_set\_event\_handler — Реєструє callback-функцію, яка буде викликатись при публікації подій

### Опис

```methodsynopsis
ibase_set_event_handler(callable $event_handler, string $event_name, string ...$even_names): resource
```

```methodsynopsis
ibase_set_event_handler(    resource $connection,    callable $event_handler,    string $event_name,    string ...$event_names): resource
```

Функція реєструє функцію PHP в якості обробника подій для зазначених подій.

### Список параметрів

`event_handler`

Callback-функція викликається з ім'ям події та ресурсом посилання як аргументи кожного разу, коли одна із зазначених подій публікується базою даних.

Callback-функція має повертати **`false`**, якщо обробник події має бути скасовано. Будь-яке інше значення, що повертається, ігнорується. Функція ухвалює до 15 аргументів події.

`event_name`

Найменування події.

`event_names`

Дозволено максимум 15 подій.

### Значення, що повертаються

Значення, що повертається, є ресурсом події. Цей ресурс можна використовувати для звільнення обробника подій за допомогою [ibase\_free\_event\_handler()](function.ibase-free-event-handler.md)

### Приклади

**Пример #1 Пример использования**ibase\_set\_event\_handler()\*\*\*\*

```php
<?php

function event_handler($event_name, $link)
{
    if ($event_name == "NEW ORDER") {
        // обрабатываем новый заказ
        ibase_query($link, "UPDATE orders SET status='handled'");
    } else if ($event_name == "DB_SHUTDOWN") {
        // отменяем обработчик событий
        return false;
    }
}

ibase_set_event_handler($link, "event_handler", "NEW_ORDER", "DB_SHUTDOWN");
?>
```

### Дивіться також

-   [ibase\_free\_event\_handler()](function.ibase-free-event-handler.md) \- скасовує зареєстрований обробник події
-   [ibase\_wait\_event()](function.ibase-wait-event.md) \- Чекаємо, поки подія буде опублікована в базі даних
