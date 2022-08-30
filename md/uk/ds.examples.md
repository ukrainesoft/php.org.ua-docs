Приклади

-   [« Обумовлені константи](ds.constants.md)
    
-   [Коллекция »](class.ds-collection.html)
    
-   [PHP Manual](index.md)
    
-   [Структури даних](book.ds.md)
    
-   Приклади
    

# Приклади

**Приклад #1 Vector**

```php
<?php

$vector = new \Ds\Vector();

$vector->push('a');
$vector->push('b', 'c');

$vector[] = 'd';

print_r($vector);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => a
    [1] => b
    [2] => c
    [3] => d
)
```

**Приклад #2 Map**

```php
<?php

$map = new \Ds\Map();

$map->put('a', 1);
$map->put('b', 2);

$map['c'] = 3;

print_r($map);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => a
            [value] => 1
        )

    [1] => Ds\Pair Object
        (
            [key] => b
            [value] => 2
        )

    [2] => Ds\Pair Object
        (
            [key] => c
            [value] => 3
        )

)
```