Відновлює початкове значення конфігураційної установки includepath

-   [« putenv](function.putenv.md)
    
-   [setincludepath »](function.set-include-path.html)
    
-   [PHP Manual](index.md)
    
-   [Опції PHP/інформаційні функції](ref.info.md)
    
-   Відновлює початкове значення конфігураційної установки includepath
    

# restoreincludepath

(PHP 4> = 4.3.0, PHP 5, PHP 7)

restoreincludepath — Відновлює початкове значення конфігураційної установки includepath

**Увага**

Ця функція *ЗАСТАРІЛА*, починаючи з PHP 7.4.0 і була *ВИДАЛЕНО*починаючи з PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
restore_include_path(): void
```

Відновлює вихідне значення конфігураційної установки [includepath](ini.core.html#ini.include-path), яка записана в php.ini

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **restoreincludepath()****

```php
<?php

echo get_include_path();  // .:/usr/local/lib/php

set_include_path('/inc');

echo get_include_path();  // /inc

restore_include_path();

// или так
ini_restore('include_path');

echo get_include_path();  // .:/usr/local/lib/php

?>
```

### Дивіться також

-   [inirestore()](function.ini-restore.html) - Відновлює налаштування конфігурації.
-   [getincludepath()](function.get-include-path.html) - Отримання поточного значення конфігураційної установки includepath
-   [setincludepath()](function.set-include-path.html) - Встановлює налаштування конфігурації includepath
-   [include](function.include.md) - include