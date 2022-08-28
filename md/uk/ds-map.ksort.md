Сортує поточну колекцію за ключами

-   [« Ds\\Map::keys](ds-map.keys.html)
    
-   [Ds\\Map::ksorted »](ds-map.ksorted.html)
    
-   [PHP Manual](index.html)
    
-   [Коллекция пар ключ-значение](class.ds-map.html)
    
-   Сортує поточну колекцію за ключами
    

# ДсMap::ksort

(PECL ds >= 1.0.0)

ДсMap::ksort — Сортує поточну колекцію за ключами

### Опис

```methodsynopsis
public Ds\Map::ksort(callable $comparator = ?): void
```

Сортує поточну колекцію за ключами, опціонально використовуючи callback-функцію `comparator` для порівняння елементів.

### Список параметрів

`comparator`

Функція порівняння повинна повертати ціле, яке менше, дорівнює чи більше нуля, якщо перший аргумент є відповідно меншим, рівним чи більшим, ніж другий.

```methodsynopsis
callback(mixed $a, mixed $b): int
```

**Застереження**

*Не ціле* значення, повернене з функції порівняння, такого як float, буде приведено до цілої кількості (int). Отже значення типу 0.99 і 0.1 будуть наведені до 0, що означатиме рівність порівнюваних значень.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсMap::ksort()****

```php
<?php
$map = new \Ds\Map(["b" => 2, "c" => 3, "a" => 1]);
$map->ksort();

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

**Приклад #2 Приклад використання **ДсMap::ksort()** з callback-функцією порівняння**

```php
<?php
$map = new \Ds\Map([1 => "x", 2 => "y", 0 => "z"]);

// Обратный порядок
$map->ksort(function($a, $b) {
    return $b <=> $a;
});

print_r($map);
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