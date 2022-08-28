Отримує попереднє встановлене значення, що повертається для функції

-   [« uopz\_get\_property](function.uopz-get-property.html)
    
-   [uopz\_get\_static »](function.uopz-get-static.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Uopz](ref.uopz.html)
    
-   Отримує попереднє встановлене значення, що повертається для функції
    

# uopzgetreturn

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopzgetreturn — Отримує попереднє встановлене значення, що повертається для функції

### Опис

```methodsynopsis
uopz_get_return(string $function): mixed
```

```methodsynopsis
uopz_get_return(string $class, string $function): mixed
```

Отримує значення, що повертається `function`, раніше встановлене за допомогою [uopz\_set\_return()](function.uopz-set-return.html)

### Список параметрів

`class`

Ім'я класу, що містить функцію

`function`

Ім'я функції

### Значення, що повертаються

Раніше встановлено значення або об'єкт Closure.

### Приклади

**Приклад #1 Приклад використання **uopzgetreturn()****

```php
<?php
uopz_set_return("strlen", 42);
echo uopz_get_return("strlen");
?>
```

Результат виконання цього прикладу:

```
42
```