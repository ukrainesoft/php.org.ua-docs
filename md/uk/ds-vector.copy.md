Повертає поверхневу копію вектора

-   [« DsVector::contains](ds-vector.contains.html)
    
-   [ДсVector::count »](ds-vector.count.html)
    
-   [PHP Manual](index.html)
    
-   [Вектор](class.ds-vector.html)
    
-   Повертає поверхневу копію вектора
    

# ДсVector::copy

(PECL ds >= 1.0.0)

ДсVector::copy — Повертає поверхневу копію вектора

### Опис

```methodsynopsis
public Ds\Vector::copy(): Ds\Vector
```

Повертає поверхневу копію вектора.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Вектор поверхнева копія.

### Приклади

**Приклад #1 Приклад використання **ДсVector::copy()****

```php
<?php
$a = new \Ds\Vector([1, 2, 3]);
$b = $a->copy();

// Изменение копии не отражается на оригинале
$b->push(4);

print_r($a);
print_r($b);
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
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
)
```