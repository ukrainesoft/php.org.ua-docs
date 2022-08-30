Створює функцію під час виконання

-   [« uopzflags](function.uopz-flags.html)
    
-   [uopzgetexitstatus »](function.uopz-get-exit-status.html)
    
-   [PHP Manual](index.html)
    
-   [Функції Uopz](ref.uopz.html)
    
-   Створює функцію під час виконання
    

# uopzfunction

(PECL uopz 1, PECL uopz 2)

uopzfunction — Створює функцію під час виконання

**Увага**

Ця функція була *ВИДАЛЕНО* у PECL uopz 5.0.0.

### Опис

```methodsynopsis
uopz_function(string $function, Closure $handler, int $modifiers = ?): void
```

```methodsynopsis
uopz_function(    string $class,    string $function,    Closure $handler,    int $modifiers = ?): void
```

Створює функцію під час виконання

### Список параметрів

`class`

Ім'я класу для отримання нової функції

`function`

Ім'я функції

`handler`

Замикання функції

`modifiers`

Модифікатори для функції, скопійовані за замовчуванням або ZENDACCPUBLIC

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **uopzfunction()****

```php
<?php
uopz_function("my_strlen", function($arg) {
    return strlen($arg);
});
echo my_strlen("Привет, Мир");
?>
```

Результат виконання цього прикладу:

```
11
```

**Приклад #2 Приклад використання **uopzfunction()** з класом**

```php
<?php
class My {}

uopz_function(My::class, "strlen", function($arg) {
    return strlen($arg);
}, ZEND_ACC_STATIC);

echo My::strlen("Привет, Мир");
?>
```

Результат виконання цього прикладу:

```
11
```