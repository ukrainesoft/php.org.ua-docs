- [« Ds\Map::ksort](ds-map.ksort.md)
- [Ds\Map::last »](ds-map.last.md)

- [PHP Manual](index.md)
- [Колекція пар ключ-значення](class.ds-map.md)
- Повертає копію колекції, відсортованої за ключами

# Ds\Map::ksorted

(No version information available, might only be in Git)

Ds\Map::ksorted — Повертає копію відсортованої колекції.

### Опис

public **Ds\Map::ksorted**([callable](language.types.callable.md)
`$comparator` = ?): [Ds\Map](class.ds-map.md)

Повертає копію колекції, відсортованої за ключами, опціонально
використовуючи callback-функцію `comparator` для порівняння елементів.

### Список параметрів

`comparator`
Функція порівняння повинна повертати ціле, яке менше, або
більше нуля, якщо перший аргумент є відповідно меншим,
рівним чи більшим, ніж другий.

callback([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$a`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$b`): int

**Застереження**
Повернення *не цілого* значення функції порівняння, такого як float,
буде приведено до цілого числа (int). Так що значення типу 0.99 та 0.1
будуть приведені до 0, що означатиме рівність порівнюваних значень.

### Значення, що повертаються

Повертає копію колекції відсортованої за ключами.

### Приклади

**Приклад #1 Приклад використання **Ds\Map::ksorted()****

` <?php$map = new \Ds\Map(["b" => 2, "c" => 3, "a" => 1]);print_r($map->ksorted());?> `

Результатом виконання цього прикладу буде щось подібне:

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

**Приклад #2 Приклад використання **Ds\Map::ksorted()** з
callback-функцією порівняння**

` <?php$map = new \Ds\Map([1 => "x", 2 => "y", 0 => "z"]);// Зворотний порядок$sorted = $map->ksorted( function($a, $b) {   return $b <=> $a;});print_r($sorted);?> `

Результатом виконання цього прикладу буде щось подібне:

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
