Перевіряє, чи є змінна ресурсом

-   [« isreal](function.is-real.html)
    
-   [ісscalar »](function.is-scalar.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи зі змінними](ref.var.html)
    
-   Перевіряє, чи є змінна ресурсом
    

# ісresource

(PHP 4, PHP 5, PHP 7, PHP 8)

ісresource — Перевіряє, чи є змінна ресурсом

### Опис

```methodsynopsis
is_resource(mixed $value): bool
```

Перевіряє, чи є змінна ресурсом (resource).

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Повертає **`true`**, якщо `value` є ресурсом (resource), або **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ісresource()****

```php
<?php

$handle = fopen("php://stdout", "w");
if (is_resource($handle)) {
    echo '$handle - это ресурс';
}
?>
```

Результат виконання цього прикладу:

```
$handle - это ресурс
```

### Примітки

> **Зауваження**
> 
> Функція **ісresource()** не робить суворої перевірки типу; вона поверне **`false`**, якщо `value` є ресурсом, який було закрито.

### Дивіться також

-   [Тип resource](language.types.resource.html)
-   [getresourcetype()](function.get-resource-type.html) - Повертає тип ресурсу