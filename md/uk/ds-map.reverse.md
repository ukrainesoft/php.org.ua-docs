- [« Ds\Map::remove](ds-map.remove.md)
- [Ds\Map::reversed »](ds-map.reversed.md)

- [PHP Manual](index.md)
- [Колекція пар ключ-значення](class.ds-map.md)
- Перевертає поточну колекцію

# Ds\Map::reverse

(PECL ds \>= 1.0.0)

Ds\Map::reverse — Перевертає поточну колекцію

### Опис

public **Ds\Map::reverse**(): void

Перевертає поточну колекцію.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **Ds\Map::reverse()****

` <?php$map = new \Ds\Map(["a" => 1, "b" => 2, c" => 3]);$map->reverse();print_r($map) ;?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Map Object
(
[0] => Ds\Pair Object
(
[key] => c
[value] => 3
)

[1] => Ds\Pair Object
(
[key] => b
[value] => 2
)

[2] => Ds\Pair Object
(
[key] => a
[value] => 1
)

)
