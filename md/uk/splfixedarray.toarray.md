Повертає звичайний PHP-масив зі значеннями фіксованого масиву

-   [« SplFixedArray::setSize](splfixedarray.setsize.md)
    
-   [SplFixedArray::valid »](splfixedarray.valid.md)
    
-   [PHP Manual](index.md)
    
-   [SplFixedArray](class.splfixedarray.md)
    
-   Повертає звичайний PHP-масив зі значеннями фіксованого масиву
    

# SplFixedArray::toArray

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SplFixedArray::toArray — Повертає звичайний PHP-масив зі значеннями фіксованого масиву

### Опис

```methodsynopsis
public SplFixedArray::toArray(): array
```

Повертає стандартний PHP-масив зі значеннями фіксованого масиву.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає PHP-масив (array), складений із значень фіксованого масиву.

### Приклади

**Приклад #1 Приклад використання **SplFixedArray::toArray()****

```php
<?php
$fa = new SplFixedArray(3);
$fa[0] = 0;
$fa[2] = 2;
var_dump($fa->toArray());
?>
```

Результат виконання цього прикладу:

```
array(3) {
  [0]=>
  int(0)
  [1]=>
  NULL
  [2]=>
  int(2)
}
```