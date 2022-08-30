Повертає копію колекції, відсортованої за ключами

-   [« DsMap::ksort](ds-map.ksort.html)
    
-   [ДсMap::last »](ds-map.last.html)
    
-   [PHP Manual](index.html)
    
-   [Коллекция пар ключ-значение](class.ds-map.html)
    
-   Повертає копію колекції, відсортованої за ключами
    

# ДсMap::ksorted

(No version information available, might only be in Git)

ДсMap::ksorted — Повертає копію колекції, відсортованої за ключами

### Опис

```methodsynopsis
public Ds\Map::ksorted(callable $comparator = ?): Ds\Map
```

Повертає копію колекції, відсортованої за ключами, опціонально використовуючи callback-функцію `comparator` для порівняння елементів.

### Список параметрів

`comparator`

Функція порівняння повинна повертати ціле, яке менше, дорівнює чи більше нуля, якщо перший аргумент є відповідно меншим, рівним чи більшим, ніж другий.

```methodsynopsis
callback(mixed $a, mixed $b): int
```

**Застереження**

Повернення *не цілого* значення функції порівняння, такого як float, буде приведено до цілого числа (int). Отже значення типу 0.99 і 0.1 будуть наведені до 0, що означатиме рівність порівнюваних значень.

### Значення, що повертаються

Повертає копію колекції відсортованої за ключами.

### Приклади

**Приклад #1 Приклад використання **ДсMap::ksorted()****

```php
<?php
$map = new \Ds\Map(["b" => 2, "c" => 3, "a" => 1]);

print_r($map->ksorted());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Map Object
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

**Приклад #2 Приклад використання **ДсMap::ksorted()** з callback-функцією порівняння**

```php
<?php
$map = new \Ds\Map([1 => "x", 2 => "y", 0 => "z"]);

// Обратный порядок
$sorted = $map->ksorted(function($a, $b) {
    return $b <=> $a;
});

print_r($sorted);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Map Object
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => 2
            [value] => y
        )

    [1] => Ds\Pair Object
        (
            [key] => 1
            [value] => x
        )

    [2] => Ds\Pair Object
        (
            [key] => 0
            [value] => z
        )

)
```