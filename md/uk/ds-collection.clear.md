Видаляє всі значення

-   [« Коллекция](class.ds-collection.html)
    
-   [ДсCollection::copy »](ds-collection.copy.html)
    
-   [PHP Manual](index.html)
    
-   [Коллекция](class.ds-collection.html)
    
-   Видаляє всі значення
    

# ДсCollection::clear

(PECL ds >= 1.0.0)

ДсCollection::clear — Видаляє всі значення

### Опис

```methodsynopsis
abstract public Ds\Collection::clear(): void
```

Видаляє всі значення колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад **ДсCollection::clear()****

```php
<?php
$collection = new \Ds\Vector([1, 2, 3]);
print_r($collection);

$collection->clear();
print_r($collection);
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