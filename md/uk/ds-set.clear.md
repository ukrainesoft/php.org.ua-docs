Видаляє всі значення з колекції

-   [« DsSet::capacity](ds-set.capacity.html)
    
-   [ДсSet::construct »](ds-set.construct.html)
    
-   [PHP Manual](index.md)
    
-   [Набор](class.ds-set.html)
    
-   Видаляє всі значення з колекції
    

# ДсSet::clear

(PECL ds >= 1.0.0)

ДсSet::clear — Видаляє всі значення з колекції

### Опис

```methodsynopsis
public Ds\Set::clear(): void
```

Видаляє всі значення колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсSet::clear()****

```php
<?php
$set = new \Ds\Set([1, 2, 3]);
print_r($set);

$set->clear();
print_r($set);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Set Object
(
    [0] => 1
    [1] => 2
    [2] => 3
)
Ds\Set Object
(
)
```