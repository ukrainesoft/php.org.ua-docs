- [«Ds\Map::putAll](ds-map.putall.md)
- [Ds\Map::remove »](ds-map.remove.md)

- [PHP Manual](index.md)
- [Колекція пар ключ-значення](class.ds-map.md)
- Зменшує колекцію до одного значення, використовуючи callback-функцію

# Ds\Map::reduce

(PECL ds \>= 1.0.0)

Ds\Map::reduce — Зменшує колекцію до одного значення, використовуючи
callback-функцію

### Опис

public **Ds\Map::reduce**([callable](language.types.callable.md)
`$callback`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$initial` = ?):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

Зменшує колекцію до одного значення, використовуючи callback-функцію.

### Список параметрів

`callback`
callback([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$carry`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$key`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$value`):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

`carry`
Значення, повернене попереднім запуском функції або initial, якщо
функцію запущено вперше.

`key`
Ключ поточної ітерації.

`value`
Значення поточної ітерації.

`initial`
Початкове значення для параметра carry. Можна вказати **`null`**.

### Значення, що повертаються

Значення, повернене остаточним запуском callback-функції.

### Приклади

**Приклад #1 Приклад використання **Ds\Map::reduce()** з початковим
значенням**

` <?php$map = new \Ds\Map(["a" => 1, "b" => 2, c" => 3]);$callback = function($carry, $key, $value ) {    return $carry * $value;};var_dump($map->reduce($callback, 5));// Ітерації://// $carry = $initial = 5/// $carry * 1 =  5// $carry = $carry * 2 = 10//$$carry = $carry * 3 = 30?> `

Результатом виконання цього прикладу буде щось подібне:

int(30)

**Приклад #2 Приклад використання **Ds\Map::reduce()** без початкового
значення**

` <?php$map = new \Ds\Map(["a" => 1, "b" => 2, c" => 3]);var_dump($map->reduce(function($carry, $key, $value) {   return $carry + $value + 5;}));// Ітерації://// $carry = $initial = null///// $carry = $car          // $carry = $carry + 2 + 5 = 13// $carry = $carry + 3 + 5 = 21?> `

Результатом виконання цього прикладу буде щось подібне:

int(21)
