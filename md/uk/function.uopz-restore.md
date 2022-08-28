Відновити раніше зарезервовану функцію

-   [« uopz\_rename](function.uopz-rename.html)
    
-   [uopz\_set\_hook »](function.uopz-set-hook.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Uopz](ref.uopz.html)
    
-   Відновити раніше зарезервовану функцію
    

# uopzrestore

(PECL uopz 1> = 1.0.3, PECL uopz 2)

uopzrestore — Відновити раніше зарезервовану функцію

**Увага**

Ця функція була *ВИДАЛЕНО* у PECL uopz 5.0.0.

### Опис

```methodsynopsis
uopz_restore(string $function): void
```

```methodsynopsis
uopz_restore(string $class, string $function): void
```

Відновити раніше зарезервовану функцію

### Список параметрів

`class`

Ім'я класу, що містить функцію відновлення

`function`

Ім'я функції

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **uopzrestore()****

```php
<?php
uopz_backup("fgets");
uopz_function("fgets", function(){
    return true;
});
var_dump(fgets());
uopz_restore('fgets');
fgets();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Warning: fgets() expects at least 1 parameter, 0 given in /path/to/script.php on line 8
```