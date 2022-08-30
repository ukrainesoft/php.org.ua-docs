Скасує раніше встановлене значення, що повертається для функції

-   [« uopzunsetmock](function.uopz-unset-mock.html)
    
-   [WinCache »](book.wincache.html)
    
-   [PHP Manual](index.html)
    
-   [Функції Uopz](ref.uopz.html)
    
-   Скасує раніше встановлене значення, що повертається для функції
    

# uopzunsetreturn

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopzunsetreturn — Скасує раніше встановлене значення, що повертається для функції

### Опис

```methodsynopsis
uopz_unset_return(string $function): bool
```

```methodsynopsis
uopz_unset_return(string $class, string $function): bool
```

Скасує значення, що повертається `function`, раніше задане функцією [uopzsetreturn()](function.uopz-set-return.html)

### Список параметрів

`class`

Ім'я класу, що містить функцію

`function`

Ім'я функції

### Значення, що повертаються

True у разі успішного виконання

### Приклади

**Приклад #1 Приклад використання **uopzunsetreturn()****

```php
<?php
uopz_set_return("strlen", 42);
$len = strlen("Banana");
uopz_unset_return("strlen");
echo $len + strlen("Banana");
?>
```

Результат виконання цього прикладу:

```
48
```