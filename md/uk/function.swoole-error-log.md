Виводить повідомлення про помилки до журналу

-   [« swooleerrno](function.swoole-errno.html)
    
-   [swooleeventadd »](function.swoole-event-add.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Swoole](ref.swoole-funcs.html)
    
-   Виводить повідомлення про помилки до журналу
    

# swooleerrorlog

(PECL swoole >= 4.5.8)

swooleerrorlog — Виводить повідомлення про помилки до журналу

### Опис

```methodsynopsis
swoole_error_log(int $level, string $msg): void
```

Виводить повідомлення про помилки до журналу.

### Список параметрів

`level`

Рівень запису в журнал можна використовувати константи: **`SWOOLE_LOG_DEBUG`** **`SWOOLE_LOG_TRACE`** **`SWOOLE_LOG_INFO`** **`SWOOLE_LOG_NOTICE`** **`SWOOLE_LOG_WARNING`** **`SWOOLE_LOG_ERROR`** **`SWOOLE_LOG_NONE`**

`msg`

Повідомлення, яке записується в журнал.

### Значення, що повертаються

Функція не повертає значення після виконання.