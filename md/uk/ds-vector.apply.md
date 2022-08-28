Оновлює всі значення, застосовуючи до них передану callback-функцію

-   [« Ds\\Vector::allocate](ds-vector.allocate.html)
    
-   [Ds\\Vector::capacity »](ds-vector.capacity.html)
    
-   [PHP Manual](index.html)
    
-   [Вектор](class.ds-vector.html)
    
-   Оновлює всі значення, застосовуючи до них передану callback-функцію
    

# ДсVector::apply

(PECL ds >= 1.0.0)

ДсVector::apply — Оновлює всі значення, застосовуючи до них передану callback-функцію

### Опис

```methodsynopsis
public Ds\Vector::apply(callable $callback): void
```

Оновлює всі значення, застосовуючи до них передану `callback`функцію.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $value): mixed
```

Об'єкт типу [callable](language.types.callable.html)

Callback-функція має повертати нове значення, яке замінить поточне.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсVector::apply()****

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);
$vector->apply(function($value) { return $value * 2; });

print_r($vector);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => 2
    [1] => 4
    [2] => 6
)
```