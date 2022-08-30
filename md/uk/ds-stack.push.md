Додає значення у стек

-   [« DsStack::pop](ds-stack.pop.html)
    
-   [ДсStack::toArray »](ds-stack.toarray.html)
    
-   [PHP Manual](index.md)
    
-   [Стек](class.ds-stack.html)
    
-   Додає значення у стек
    

# ДсStack::push

(PECL ds >= 1.0.0)

ДсStack::push — Додає значення до стек

### Опис

```methodsynopsis
public Ds\Stack::push(mixed ...$values): void
```

Додає значення `values` у стек

### Список параметрів

`values`

Значення, що додаються.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсStack::push()****

```php
<?php
$stack = new \Ds\Stack();

$stack->push("a");
$stack->push("b");
$stack->push("c", "d");
$stack->push(...["e", "f"]);

print_r($stack);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Stack Object
(
    [0] => a
    [1] => b
    [2] => c
    [3] => d
    [4] => e
    [5] => f
)
```