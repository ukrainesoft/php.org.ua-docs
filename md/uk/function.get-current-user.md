Отримує ім'я власника поточного скрипту PHP

-   [« get\_cfg\_var](function.get-cfg-var.html)
    
-   [get\_defined\_constants »](function.get-defined-constants.html)
    
-   [PHP Manual](index.html)
    
-   [Опции PHP/информационные функции](ref.info.html)
    
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

-   [getmyuid()](function.getmyuid.html) - Отримання UID власника скрипта PHP
-   [getmygid()](function.getmygid.html) - Отримати GID власника скрипта PHP
-   [getmypid()](function.getmypid.html) - Отримання ID процесу PHP
-   [getmyinode()](function.getmyinode.html) - Отримує значення inode поточного скрипту
-   [getlastmod()](function.getlastmod.html) - Отримує час останньої модифікації сторінки