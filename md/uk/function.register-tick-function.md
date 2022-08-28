Реєструє функцію для виконання при кожному тику

-   [« register\_shutdown\_function](function.register-shutdown-function.html)
    
-   [unregister\_tick\_function »](function.unregister-tick-function.html)
    
-   [PHP Manual](index.html)
    
-   [Функции управления функциями](ref.funchand.html)
    
-   Реєструє функцію для виконання при кожному тику
    

# registertickfunction

(PHP 4> = 4.0.3, PHP 5, PHP 7, PHP 8)

registertickfunction — Реєструє функцію для виконання при кожному тику

### Опис

```methodsynopsis
register_tick_function(callable $callback, mixed ...$args): bool
```

Реєструє функцію `callback`, яка повинна викликатись при кожному [тике](control-structures.declare.html#control-structures.declare.ticks)

### Список параметрів

`callback`

Реєстрована функція.

`args`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **registertickfunction()****

```php
<?php
declare(ticks=1);

// использование функции в качестве обратного вызова
register_tick_function('my_function', true);

// использование метода объекта
$object = new my_class();
register_tick_function(array($object, 'my_method'), true);
?>
```

### Дивіться також

-   [declare](control-structures.declare.html)
-   [unregister\_tick\_function()](function.unregister-tick-function.html) - Видаляє функцію зі списку зареєстрованих для виконання на кожному тику