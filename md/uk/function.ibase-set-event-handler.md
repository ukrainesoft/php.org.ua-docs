Реєструє callback-функцію, яка буде викликатись при публікації подій

-   [« ibaseservicedetach](function.ibase-service-detach.html)
    
-   [ibasetrans »](function.ibase-trans.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Firebird/InterBase](ref.ibase.md)
    
-   Реєструє callback-функцію, яка буде викликатись при публікації подій
    

# ibaseseteventhandler

(PHP 5, PHP 7 < 7.4.0)

ibaseseteventhandler — Реєструє callback-функцію, яка буде викликатись при публікації подій

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

Значення, що повертається, є ресурсом події. Цей ресурс можна використовувати для звільнення обробника подій за допомогою [ibasefreeeventhandler()](function.ibase-free-event-handler.html)

### Приклади

**Приклад #1 Приклад використання **ibaseseteventhandler()****

```php
<?php

function event_handler($event_name, $link)
{
    if ($event_name == "NEW ORDER") {
        // обрабатываем новый заказ
        ibase_query($link, "UPDATE orders SET status='handled'");
    } else if ($event_name == "DB_SHUTDOWN") {
        // отменяем обработчик событий
        return false;
    }
}

ibase_set_event_handler($link, "event_handler", "NEW_ORDER", "DB_SHUTDOWN");
?>
```

### Дивіться також

-   [ibasefreeeventhandler()](function.ibase-free-event-handler.html) - скасовує зареєстрований обробник події
-   [ibasewaitevent()](function.ibase-wait-event.html) - Чекаємо, поки подія буде опублікована в базі даних