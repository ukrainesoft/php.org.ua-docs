Повертає поточну версію модуля Stomp

-   [« stompconnecterror](function.stomp-connect-error.html)
    
-   [Stomp »](class.stomp.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Stomp](ref.stomp.html)
    
-   Повертає поточну версію модуля Stomp
    

# stompversion

(PECL stomp >= 0.1.0)

stompversion — Повертає поточну версію модуля Stomp

### Опис

```methodsynopsis
stomp_version(): string
```

Повертає рядок, який містить версію поточного модуля Stomp.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає поточну версію модуля Stomp

### Приклади

**Приклад #1 Приклад використання **stompversion()****

```php
<?php

var_dump(stomp_version());

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(5) "0.2.0"
```