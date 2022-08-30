Скасує реєстрацію обгортки URL

-   [« streamwrapperrestore](function.stream-wrapper-restore.html)
    
-   [Swoole »](book.swoole.md)
    
-   [PHP Manual](index.md)
    
-   [Функції для роботи з потоками](ref.stream.md)
    
-   Скасує реєстрацію обгортки URL
    

# streamwrapperunregister

(PHP 5> = 5.1.0, PHP 7, PHP 8)

streamwrapperunregister — Скасує реєстрацію обгортки URL

### Опис

```methodsynopsis
stream_wrapper_unregister(string $protocol): bool
```

Дозволяє вам вимкнути вже певну обгортку потоку. Як тільки обгортка буде вимкнена, ви можете перезаписати її обгорткою користувача, використовуючи [streamwrapperregister()](function.stream-wrapper-register.html) або включити її повторно, використовуючи [streamwrapperrestore()](function.stream-wrapper-restore.html)

### Список параметрів

`protocol`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.