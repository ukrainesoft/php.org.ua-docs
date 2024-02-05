---
navigation:
  - ds.constants.md: « Зумовлені константи
  - class.ds-collection.md: Ds\\Collection »
  - index.md: PHP Manual
  - book.ds.md: Структури даних
title: Приклади
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Приклади

**Приклад #1 Vector**

```php
<?php

$vector = new \Ds\Vector();

$vector->push('a');
$vector->push('b', 'c');

$vector[] = 'd';

print_r($vector);

?>
```

Висновок наведеного прикладу буде схожим на:

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

$map = new \Ds\Map();

$map->put('a', 1);
$map->put('b', 2);

$map['c'] = 3;

print_r($map);

?>
```

Висновок наведеного прикладу буде схожим на:

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
