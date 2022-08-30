Відновлює скасовану раніше вбудовану обгортку

-   [« streamwrapperregister](function.stream-wrapper-register.html)
    
-   [streamwrapperunregister »](function.stream-wrapper-unregister.html)
    
-   [PHP Manual](index.md)
    
-   [Функції для роботи з потоками](ref.stream.md)
    
-   Відновлює скасовану раніше вбудовану обгортку
    

# streamwrapperrestore

(PHP 5> = 5.1.0, PHP 7, PHP 8)

streamwrapperrestore — Відновлює скасовану вбудовану обгортку.

### Опис

```methodsynopsis
stream_wrapper_restore(string $protocol): bool
```

Відновлює вбудовану обгортку, реєстрацію якої раніше було скасовано за допомогою [streamwrapperunregister()](function.stream-wrapper-unregister.html)

### Список параметрів

`protocol`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.