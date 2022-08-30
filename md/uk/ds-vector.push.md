Додає значення до кінця вектора

-   [« DsVector::pop](ds-vector.pop.html)
    
-   [ДсVector::reduce »](ds-vector.reduce.html)
    
-   [PHP Manual](index.md)
    
-   [Вектор](class.ds-vector.html)
    
-   Додає значення до кінця вектора
    

# ДсVector::push

(PECL ds >= 1.0.0)

ДсVector::push — Додає значення до кінця вектора.

### Опис

```methodsynopsis
public Ds\Vector::push(mixed ...$values): void
```

Додає значення до кінця вектора.

### Список параметрів

`values`

Значення, що додаються.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсVector::push()****

```php
<?php
$vector = new \Ds\Vector();

$vector->push("a");
$vector->push("b");
$vector->push("c", "d");
$vector->push(...["e", "f"]);

print_r($vector);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => a
    [1] => b
    [2] => c
    [3] => d
    [4] => e
    [5] => f
)
```