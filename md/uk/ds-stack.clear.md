Видаляє всі значення з колекції

-   [« DsStack::capacity](ds-stack.capacity.html)
    
-   [ДсStack::construct »](ds-stack.construct.html)
    
-   [PHP Manual](index.md)
    
-   [Стек](class.ds-stack.html)
    
-   Видаляє всі значення з колекції
    

# ДсStack::clear

(PECL ds >= 1.0.0)

ДсStack::clear — Видаляє всі значення з колекції

### Опис

```methodsynopsis
public Ds\Stack::clear(): void
```

Видаляє всі значення колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсStack::clear()****

```php
<?php
$stack = new \Ds\Stack([1, 2, 3]);
print_r($stack);

$stack->clear();
print_r($stack);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Stack Object
(
    [0] => 3
    [1] => 2
    [2] => 1
)
Ds\Stack Object
(
)
```