- [« Ds\Map::sort](ds-map.sort.md)
- [Ds\Map::sum »](ds-map.sum.md)

- [PHP Manual](index.md)
- [Колекція пар ключ-значення](class.ds-map.md)
- Повертає відсортовану за значенням копію колекції

# Ds\Map::sorted

(PECL ds \>= 1.0.0)

Ds\Map::sorted — Повертає копію колекції, відсортовану за значенням.

### Опис

public **Ds\Map::sorted**([callable](language.types.callable.md)
`$comparator` = ?): [Ds\Map](class.ds-map.md)

Повертає відсортовану за значенням копію колекції, необов'язково
використовуючи callback-функцію `comparator`.

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
*Не ціле* значення, повернене з функції порівняння, такого як
float, буде приведено до цілої кількості (int). Отже значення типу 0.99
і 0.1 будуть наведені до 0, що означатиме рівність порівнюваних
значень.

### Значення, що повертаються

Повертає копію колекції, відсортовану за значенням.

### Приклади

**Приклад #1 Приклад використання [Ds\Map::sort()](ds-map.sort.md)**

` <?php$map = new \Ds\Map(["a" => 2, "b" => 3, "c" => 1]);print_r($map->sorted());?> `

Результатом виконання цього прикладу буде щось подібне:

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

**Приклад #2 Приклад використання [Ds\Map::sort()](ds-map.sort.md) з
callback-функцією порівняння**

` <?php$map = new \Ds\Map(["a" => 2, "b" => 3, c" => 1]);// Reverse$sorted = $map->sorted(function ($a, $b) {   return $b <=> $a;});print_r($sorted);?> `

Результатом виконання цього прикладу буде щось подібне:

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
