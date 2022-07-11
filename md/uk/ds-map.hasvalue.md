- [« Ds\Map::hasKey](ds-map.haskey.md)
- [Ds\Map::intersect »](ds-map.intersect.md)

- [PHP Manual](index.md)
- [Колекція пар ключ-значення](class.ds-map.md)
- Перевіряє, чи колекція містить задане значення

# Ds\Map::hasValue

(PECL ds \>= 1.0.0)

Ds\Map::hasValue — Перевіряє, чи колекція містить задане значення

### Опис

public
**Ds\Map::hasValue**([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$value`): bool

Перевіряє, чи колекція містить задане значення.

### Список параметрів

`value`
Значення для перевірки.

### Значення, що повертаються

Повертає **`true`**, якщо ключ знайдений, інакше **`false`**.

### Приклади

**Приклад #1 Приклад використання **Ds\Map::hasValue()****

` <?php$map = new \Ds\Map(["a" => 1, "b" => 2, c" => 3]);var_dump($map->hasValue(1)); // Truevar_dump ($ map-> has Value (4)); // false?> `

Результатом виконання цього прикладу буде щось подібне:

bool(true)
bool(false)
