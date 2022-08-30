Повертає перегорнуту копію вектора

-   [« DsVector::reverse](ds-vector.reverse.html)
    
-   [ДсVector::rotate »](ds-vector.rotate.html)
    
-   [PHP Manual](index.html)
    
-   [Вектор](class.ds-vector.html)
    
-   Повертає перегорнуту копію вектора
    

# ДсVector::reversed

(PECL ds >= 1.0.0)

ДсVector::reverse — Повертає перегорнуту копію вектора

### Опис

```methodsynopsis
public Ds\Vector::reversed(): Ds\Vector
```

Повертає перегорнуту копію вектора.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Вектор перевернена копія.

> **Зауваження**
> 
> Поточний вектор не зміниться.

### Приклади

**Приклад #1 Приклад використання **ДсVector::reversed()****

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);

print_r($vector->reversed());
print_r($vector);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => c
    [1] => b
    [2] => a
)
Ds\Vector Object
(
    [0] => a
    [1] => b
    [2] => c
)
```