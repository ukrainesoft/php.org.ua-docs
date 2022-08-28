Додати callback-функцію до наступного циклу подій

-   [« swoole\_event\_add](function.swoole-event-add.html)
    
-   [swoole\_event\_del »](function.swoole-event-del.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Swoole](ref.swoole-funcs.html)
    
-   Додати callback-функцію до наступного циклу подій
    

# swooleeventdefer

(PECL swoole >= 1.9.0)

swooleeventdefer — Додати callback-функцію до наступного циклу подій

### Опис

```methodsynopsis
swoole_event_defer(callable $callback): bool
```

### Список параметрів

`callback`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.