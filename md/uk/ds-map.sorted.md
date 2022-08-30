Повертає відсортовану за значенням копію колекції

-   [« DsMap::sort](ds-map.sort.html)
    
-   [ДсMap::sum »](ds-map.sum.html)
    
-   [PHP Manual](index.html)
    
-   [Коллекция пар ключ-значение](class.ds-map.html)
    
-   Повертає відсортовану за значенням копію колекції
    

# ДсMap::sorted

(PECL ds >= 1.0.0)

ДсMap::sorted — Повертає копію колекції, відсортовану за значенням.

### Опис

```methodsynopsis
public Ds\Map::sorted(callable $comparator = ?): Ds\Map
```

Повертає відсортовану за значенням копію колекції, необов'язково використовуючи callback-функцію `comparator`

### Список параметрів

`comparator`

Функція порівняння повинна повертати ціле, яке менше, дорівнює чи більше нуля, якщо перший аргумент є відповідно меншим, рівним чи більшим, ніж другий.

```methodsynopsis
callback(mixed $a, mixed $b): int
```

**Застереження**

*Не ціле* значення, повернене з функції порівняння, такого як float, буде приведено до цілої кількості (int). Отже значення типу 0.99 і 0.1 будуть наведені до 0, що означатиме рівність порівнюваних значень.

### Значення, що повертаються

Повертає копію колекції, відсортовану за значенням.

### Приклади

**Приклад #1 Приклад використання [ДсMap::sort()](ds-map.sort.html)**

```php
<?php
$map = new \Ds\Map(["a" => 2, "b" => 3, "c" => 1]);

print_r($map->sorted());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => c
            [value] => 1
        )

    [1] => Ds\Pair Object
        (
            [key] => a
            [value] => 2
        )

    [2] => Ds\Pair Object
        (
            [key] => b
            [value] => 3
        )

)
```

**Приклад #2 Приклад використання [ДсMap::sort()](ds-map.sort.html) з callback-функцією порівняння**

```php
<?php
$map = new \Ds\Map(["a" => 2, "b" => 3, "c" => 1]);

// Reverse
$sorted = $map->sorted(function($a, $b) {
    return $b <=> $a;
});

print_r($sorted);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => b
            [value] => 3
        )

    [1] => Ds\Pair Object
        (
            [key] => a
            [value] => 2
        )

    [2] => Ds\Pair Object
        (
            [key] => c
            [value] => 1
        )

)
```