Створює новий екземпляр класу

-   [« DsSet::clear](ds-set.clear.html)
    
-   [ДсSet::contains »](ds-set.contains.html)
    
-   [PHP Manual](index.html)
    
-   [Набор](class.ds-set.html)
    
-   Створює новий екземпляр класу
    

# ДсSet::construct

(PECL ds >= 1.0.0)

ДсSet::construct — Створює новий екземпляр класу

### Опис

public **ДсSet::construct**[mixed](language.types.declarations.html#language.types.declarations.mixed) `$values`

Створює новий екземпляр класу, використовуючи або об'єкт, що реалізує [traversable](class.traversable.html), або масив, передані як параметр `values`

### Список параметрів

`values`

Об'єкт, що реалізує інтерфейс traversable або масив.

### Приклади

**Приклад #1 Приклад використання **ДсSet::construct()****

```php
<?php
$set = new \Ds\Set();
var_dump($set);

$set = new \Ds\Set([1, 2, 3]);
var_dump($set);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Set)#1 (0) {
}
object(Ds\Set)#2 (3) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
}
```