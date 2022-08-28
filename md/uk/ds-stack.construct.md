Створює новий екземпляр класу

-   [« Ds\\Stack::clear](ds-stack.clear.html)
    
-   [Ds\\Stack::copy »](ds-stack.copy.html)
    
-   [PHP Manual](index.html)
    
-   [Стек](class.ds-stack.html)
    
-   Створює новий екземпляр класу
    

# ДсStack::construct

(PECL ds >= 1.0.0)

ДсStack::construct — Створює новий екземпляр класу

### Опис

public **ДсStack::construct**[mixed](language.types.declarations.html#language.types.declarations.mixed) `$values`

Створює новий екземпляр класу, використовуючи або об'єкт, що реалізує [traversable](class.traversable.html), або масив, передані як параметр `values`

### Список параметрів

`values`

Об'єкт, що реалізує інтерфейс traversable або масив.

### Приклади

**Приклад #1 Приклад використання **ДсStack::construct()****

```php
<?php
$stack = new \Ds\Stack();
print_r($stack);

$stack = new \Ds\Stack([1, 2, 3]);
print_r($stack);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Stack Object
(
)
Ds\Stack Object
(
    [0] => 3
    [1] => 2
    [2] => 1
)
```