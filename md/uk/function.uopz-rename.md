Перейменувати функцію під час виконання

-   [« uopz\_redefine](function.uopz-redefine.html)
    
-   [uopz\_restore »](function.uopz-restore.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Uopz](ref.uopz.html)
    
-   Перейменувати функцію під час виконання
    

# uopzrename

(PECL uopz 1, PECL uopz 2)

uopzrename — Перейменувати функцію під час виконання

**Увага**

Ця функція була *ВИДАЛЕНО* у PECL uopz 5.0.0.

### Опис

```methodsynopsis
uopz_rename(string $function, string $rename): void
```

```methodsynopsis
uopz_rename(string $class, string $function, string $rename): void
```

Перейменовує функцію `function` на `rename`

> **Зауваження**
> 
> Якщо обидві функції існують, ця функція по суті змінює імена

### Список параметрів

`class`

Ім'я класу, що містить функцію

`function`

Ім'я існуючої функції

`rename`

Нове ім'я функції

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **uopzrename()****

```php
<?php
uopz_rename("strlen", "original_strlen");

echo original_strlen("Hello World");
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
11
```

**Приклад #2 Приклад використання **uopzrename()** з класом**

```php
<?php
class My {
    public function strlen($arg) {
        return strlen($arg);
    }
}

uopz_rename(My::class, "strlen", "original_strlen");

echo My::original_strlen("Hello World");
?>
```

Результат виконання цього прикладу:

```
11
```