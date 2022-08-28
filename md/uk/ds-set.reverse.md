Перевертає поточну колекцію

-   [« Ds\\Set::remove](ds-set.remove.html)
    
-   [Ds\\Set::reversed »](ds-set.reversed.html)
    
-   [PHP Manual](index.html)
    
-   [Набор](class.ds-set.html)
    
-   Перевертає поточну колекцію
    

# ДсSet::reverse

(PECL ds >= 1.0.0)

ДсSet::reverse — Перевертає поточну колекцію

### Опис

```methodsynopsis
public Ds\Set::reverse(): void
```

Перевертає поточну колекцію.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсSet::reverse()****

```php
<?php
$set = new \Ds\Set(["a", "b", "c"]);
$set->reverse();

print_r($set);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Set Object
(
    [0] => c
    [1] => b
    [2] => a
)
```