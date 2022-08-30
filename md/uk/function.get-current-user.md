Отримує ім'я власника поточного скрипту PHP

-   [« getcfgvar](function.get-cfg-var.html)
    
-   [getdefinedconstants »](function.get-defined-constants.html)
    
-   [PHP Manual](index.md)
    
-   [Опції PHP/інформаційні функції](ref.info.md)
    
-   Отримує ім'я власника поточного скрипту PHP
    

# getcurrentuser

(PHP 4, PHP 5, PHP 7, PHP 8)

getcurrentuser — Отримує ім'я власника поточного скрипту PHP

### Опис

```methodsynopsis
get_current_user(): string
```

Повертає ім'я власника поточного PHP-скрипту.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я користувача у вигляді рядка.

### Приклади

**Приклад #1 Приклад використання **getcurrentuser()****

```php
<?php
echo 'Текущий владелец скрипта: ' . get_current_user();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Текущий владелец скрипта: SYSTEM
```

### Дивіться також

-   [getmyuid()](function.getmyuid.md) - Отримання UID власника скрипта PHP
-   [getmygid()](function.getmygid.md) - Отримати GID власника скрипта PHP
-   [getmypid()](function.getmypid.md) - Отримання ID процесу PHP
-   [getmyinode()](function.getmyinode.md) - Отримує значення inode поточного скрипту
-   [getlastmod()](function.getlastmod.md) - Отримує час останньої модифікації сторінки