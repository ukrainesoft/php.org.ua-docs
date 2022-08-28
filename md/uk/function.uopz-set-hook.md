Встановлює обробник для виконання під час виклику функції або методу

-   [« uopz\_restore](function.uopz-restore.html)
    
-   [uopz\_set\_mock »](function.uopz-set-mock.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Uopz](ref.uopz.html)
    
-   Встановлює обробник для виконання під час виклику функції або методу
    

# uopzsethook

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopzsethook — Встановлює обробник для виконання під час виклику функції або методу

### Опис

```methodsynopsis
uopz_set_hook(string $function, Closure $hook): bool
```

```methodsynopsis
uopz_set_hook(string $class, string $function, Closure $hook): bool
```

Встановлює обробник для виконання під час виклику функції або методу.

### Список параметрів

`class`

Назва класу.

`function`

Ім'я функції чи методу.

`hook`

Замикання, яке виконується під час виклику функції або методу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Просте використання **uopzsethook()****

```php
<?php
function foo() {
    echo 'foo';
}
uopz_set_hook('foo', function () {echo 'bar';});
foo();
?>
```

Результат виконання цього прикладу:

```
barfoo
```

### Дивіться також

-   [uopz\_get\_hook()](function.uopz-get-hook.html) - отримує раніше встановлений обробник на функцію або метод
-   [uopz\_unset\_hook()](function.uopz-unset-hook.html) - Видаляє раніше встановлену функцію чи метод