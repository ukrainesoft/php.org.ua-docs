Видаляє всі значення

-   [« Ds\\Vector::capacity](ds-vector.capacity.html)
    
-   [Ds\\Vector::\_\_construct »](ds-vector.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Вектор](class.ds-vector.html)
    
-   Видаляє всі значення
    

# ДсVector::clear

(PECL ds >= 1.0.0)

ДсVector::clear — Видаляє всі значення

### Опис

```methodsynopsis
public Ds\Vector::clear(): void
```

Видаляє всі значення вектора.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсVector::clear()****

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);
print_r($vector);

$vector->clear();
print_r($vector);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => 1
    [1] => 2
    [2] => 3
)
Ds\Vector Object
(
)
```