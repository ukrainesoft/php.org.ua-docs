- [«Ds\Map::diff](ds-map.diff.md)
- [Ds\Map::first »](ds-map.first.md)

- [PHP Manual](index.md)
- [Колекція пар ключ-значення](class.ds-map.md)
- Створює нову колекцію пар із елементів, вибраних за допомогою
заданої callback-функції

# Ds\Map::filter

(PECL ds \>= 1.0.0)

Ds\Map::filter — Створює нову колекцію пар з елементів, вибраних з
допомогою заданої callback-функції

### Опис

public **Ds\Map::filter**([callable](language.types.callable.md)
`$callback` = ?): [Ds\Map](class.ds-map.md)

Створює нову колекцію пар із елементів, вибраних за допомогою заданої
callback-функції.

### Список параметрів

`callback`
callback([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$key`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$value`): bool

Опціональний аргумент типу [callable](language.types.callable.md),
який повертає **`true`**, якщо пара повинна бути включена та
**`false`**, якщо ні.

Якщо callback-функція не задана, будуть включені тільки елементи,
які наводяться до логічного значення **`true`** (дивіться розділ з
[приведенням до boolean](language.types.boolean.md#language.types.boolean.casting)).

### Значення, що повертаються

Нова колекція пар, що містить значення, для яких `callback` -функція
повернула **`true`**, або всі елементи, які при приведенні до
логічного типу стають **`true`**, якщо параметр `callback` не
заданий.

### Приклади

**Приклад #1 Приклад **Ds\Map::filter()** з використанням
callback-функції**

` <?php$map = new \Ds\Map(["a", "b", "c", "d", "e"]);var_dump($map->filter(function($key, $) value) {    return $key % 2 == 0;}));?> `

Результатом виконання цього прикладу буде щось подібне:

object(Ds\Map)#3 (3) {
[0]=>
object(Ds\Pair)#2 (2) {
["key"]=>
int(0)
["value"]=>
string(1) "a"
}
[1]=>
object(Ds\Pair)#4 (2) {
["key"]=>
int(2)
["value"]=>
string(1) "c"
}
[2]=>
object(Ds\Pair)#5 (2) {
["key"]=>
int(4)
["value"]=>
string(1) "e"
}
}

**Приклад #2 Приклад **Ds\Map::filter()** без callback-функції**

` <?php$map = new \Ds\Map(["a" => 0, "b" => 1, "c" => true, "d" => false]);var_dump($map-> filter());?> `

Результатом виконання цього прикладу буде щось подібне:

object(Ds\Map)#2 (3) {
[0]=>
int(1)
[1]=>
string(1) "a"
[2]=>
bool(true)
}
