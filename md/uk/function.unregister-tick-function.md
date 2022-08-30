Видаляє функцію зі списку зареєстрованих для виконання на кожному тику

-   [« registertickfunction](function.register-tick-function.html)
    
-   [Quickhash »](book.quickhash.html)
    
-   [PHP Manual](index.html)
    
-   [Функции управления функциями](ref.funchand.html)
    
-   Видаляє функцію зі списку зареєстрованих для виконання на кожному тику
    

# unregistertickfunction

(PHP 4> = 4.0.3, PHP 5, PHP 7, PHP 8)

unregistertickfunction — Видалення функції зі списку зареєстрованих для виконання на кожному тику

### Опис

```methodsynopsis
unregister_tick_function(callable $callback): void
```

Видаляє `function` зі списку функцій, так що вона більше не виконується при кожному тику (дивіться [tick](control-structures.declare.html)

### Список параметрів

`callback`

Функція, що видаляється.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [registertickfunction()](function.register-tick-function.html) - Реєструє функцію для виконання при кожному тику