Отримує раніше встановлений обробник на функцію чи метод

-   [« uopz\_get\_exit\_status](function.uopz-get-exit-status.html)
    
-   [uopz\_get\_mock »](function.uopz-get-mock.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Uopz](ref.uopz.html)
    
-   Отримує раніше встановлений обробник на функцію чи метод
    

# uopzgethook

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopzgethook — Отримує раніше встановлений обробник на функцію або метод

### Опис

```methodsynopsis
uopz_get_hook(string $function): Closure
```

```methodsynopsis
uopz_get_hook(string $class, string $function): Closure
```

Отримує встановлений обробник на функцію або метод.

### Список параметрів

`class`

Назва класу.

`function`

Ім'я функції чи методу.

### Значення, що повертаються

Повертає раніше встановлений обробник на функцію або метод, або **`null`**якщо обробник не був встановлений.

### Приклади

**Приклад #1 Просте використання **uopzgethook()****

```php
<?php
function foo() {
    echo 'foo';
}
uopz_set_hook('foo', function () {echo 'bar';});
var_dump(uopz_get_hook('foo'));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Closure)#2 (0) {
}
```

### Дивіться також

-   [uopz\_set\_hook()](function.uopz-set-hook.html) - Встановлює обробник для виконання під час виклику функції або методу
-   [uopz\_unset\_hook()](function.uopz-unset-hook.html) - Видаляє раніше встановлену функцію чи метод