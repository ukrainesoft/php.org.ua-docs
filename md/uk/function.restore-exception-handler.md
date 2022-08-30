Відновлює попередній обробник винятків

-   [« restoreerrorhandler](function.restore-error-handler.html)
    
-   [seterrorhandler »](function.set-error-handler.html)
    
-   [PHP Manual](index.html)
    
-   [Функции обработки ошибок](ref.errorfunc.html)
    
-   Відновлює попередній обробник винятків
    

# restoreexceptionhandler

(PHP 5, PHP 7, PHP 8)

restoreexceptionhandler — Відновлює попередній обробник винятків

### Опис

```methodsynopsis
restore_exception_handler(): bool
```

Використовується після зміни обробника виключень функцією [setexceptionhandler()](function.set-exception-handler.html), щоб повернути попередній обробник (який може бути як вбудованою функцією, так і певною користувачем).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ця функція завжди повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **restoreexceptionhandler()****

```php
<?php
    function exception_handler_1(Exception $e)
    {
        echo '[' . __FUNCTION__ . '] ' . $e->getMessage();
    }

    function exception_handler_2(Exception $e)
    {
        echo '[' . __FUNCTION__ . '] ' . $e->getMessage();
    }

    set_exception_handler('exception_handler_1');
    set_exception_handler('exception_handler_2');

    restore_exception_handler();

    throw new Exception('Вызван первый обработчик исключений...');
?>
```

Результат виконання цього прикладу:

```
[exception_handler_1] Вызван первый обработчик исключений...
```

### Дивіться також

-   [setexceptionhandler()](function.set-exception-handler.html) - Задає користувальницький обробник винятків
-   [seterrorhandler()](function.set-error-handler.html) - Задає користувальницький обробник помилок
-   [restoreerrorhandler()](function.restore-error-handler.html) - Відновлює попередній обробник помилок
-   [errorreporting()](function.error-reporting.html) - Задає, які помилки PHP потраплять у звіт