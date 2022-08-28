Скасує реєстрацію обгортки URL

-   [« stream\_wrapper\_restore](function.stream-wrapper-restore.html)
    
-   [Swoole »](book.swoole.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с потоками](ref.stream.html)
    
-   Скасує реєстрацію обгортки URL
    

# streamwrapperunregister

(PHP 5> = 5.1.0, PHP 7, PHP 8)

streamwrapperunregister — Скасує реєстрацію обгортки URL

### Опис

```methodsynopsis
stream_wrapper_unregister(string $protocol): bool
```

Дозволяє вам вимкнути вже певну обгортку потоку. Як тільки обгортка буде вимкнена, ви можете перезаписати її обгорткою користувача, використовуючи [stream\_wrapper\_register()](function.stream-wrapper-register.html) або включити її повторно, використовуючи [stream\_wrapper\_restore()](function.stream-wrapper-restore.html)

### Список параметрів

`protocol`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.