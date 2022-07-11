- [« Ds\Map::\_\_construct](ds-map.construct.md)
- [Ds\Map::count »](ds-map.count.md)

- [PHP Manual](index.md)
- [Колекція пар ключ-значення](class.ds-map.md)
- Повертає поверхневу копію колекції

# Ds\Map::copy

(PECL ds \>= 1.0.0)

Ds\Map::copy — Повертає поверхневу копію колекції

### Опис

public **Ds\Map::copy**(): [Ds\Map](class.ds-map.md)

Повертає поверхневу копію колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Колекція поверхнева копія.

### Приклади

**Приклад #1 Приклад використання **Ds\Map::copy()****

` <?php$map = new \Ds\Map([   "a" => 1,   "b" => 2,   "c" => 3,]);print_r($map->copy()); > `

Результатом виконання цього прикладу буде щось подібне:

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
