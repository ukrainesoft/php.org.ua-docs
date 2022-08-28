Перевантажити опкод VM

-   [« uopz\_implement](function.uopz-implement.html)
    
-   [uopz\_redefine »](function.uopz-redefine.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Uopz](ref.uopz.html)
    
-   Перевантажити опкод VM
    

# uopzoverload

(PECL uopz 1, PECL uopz 2)

uopzoverload — Перевантажити опкод VM

**Увага**

Ця функція була *ВИДАЛЕНО* у PECL uopz 5.0.0.

### Опис

```methodsynopsis
uopz_overload(int $opcode, Callable $callable): void
```

Перевантажує певний `opcode` за допомогою функції користувача

### Список параметрів

`opcode`

Коректний опкод, дивіться константи для отримання опкодів, що підтримуються

`callable`

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **uopzoverload()****

```php
<?php
uopz_overload(ZEND_EXIT, function(){});

exit();
echo "Привет, Мир";
?>
```

Результат виконання цього прикладу:

```
Привет, Мир
```