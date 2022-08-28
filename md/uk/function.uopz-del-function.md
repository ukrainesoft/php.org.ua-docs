Видаляє раніше додану функцію або метод

-   [« uopz\_copy](function.uopz-copy.html)
    
-   [uopz\_delete »](function.uopz-delete.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Uopz](ref.uopz.html)
    
-   Видаляє раніше додану функцію або метод
    

# uopzdelfunction

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopzdelfunction — Видалення раніше доданої функції або методу

### Опис

```methodsynopsis
uopz_del_function(string $function): bool
```

```methodsynopsis
uopz_del_function(string $class, string $function, int &$all = true): bool
```

Видалення раніше доданої функції або методу.

### Список параметрів

`class`

Назва класу.

`function`

Ім'я функції чи методу.

`all`

Чи торкнуться всі класи, які походять від класу (`class`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

**uopzdelfunction()** викидає [RuntimeException](class.runtimeexception.html), якщо видалені функції або метод не були додані за допомогою [uopz\_add\_function()](function.uopz-add-function.html)

### Приклади

**Приклад #1 Просте використання **uopzdelfunction()****

```php
<?php
uopz_add_function('foo', function () {echo 'bar';});
var_dump(function_exists('foo'));
uopz_del_function('foo');
var_dump(function_exists('foo'));
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(false)
```

### Дивіться також

-   [uopz\_add\_function()](function.uopz-add-function.html) - Додає неіснуючу функцію чи метод
-   [uopz\_unset\_return()](function.uopz-unset-return.html) - Скасує раніше встановлене значення, що повертається для функції