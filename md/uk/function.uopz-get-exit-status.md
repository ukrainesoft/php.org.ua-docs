Отримати останній встановлений статус виходу

-   [« uopzfunction](function.uopz-function.html)
    
-   [uopzgethook »](function.uopz-get-hook.html)
    
-   [PHP Manual](index.html)
    
-   [Функції Uopz](ref.uopz.html)
    
-   Отримати останній встановлений статус виходу
    

# uopzgetexitstatus

(PECL uopz 5, PECL uopz, PECL uopz 7)

uopzgetexitstatus — Отримати останній встановлений статус виходу

### Опис

```methodsynopsis
uopz_get_exit_status(): mixed
```

Отримує останній встановлений статус виходу, тобто значення, передане в [exit()](function.exit.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ця функція повертає останній статус виходу або **`null`**, якщо [exit()](function.exit.html) не було викликано.

### Приклади

**Приклад #1 Приклад використання **uopzgetexitstatus()****

```php
<?php
exit(123);
echo uopz_get_exit_status();?>
```

Результат виконання цього прикладу:

```
123
```

### Примітки

**Застереження**

[OPcache](book.opcache.html) оптимізує мертвий код після завершення.

### Дивіться також

-   [uopzallowexit()](function.uopz-allow-exit.html) - Дозволяє керувати вимкненим опкодом exit