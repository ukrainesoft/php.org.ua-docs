- [« Ds\Map::pairs](ds-map.pairs.md)
- [Ds\Map::putAll »](ds-map.putall.md)

- [PHP Manual](index.md)
- [Колекція пар ключ-значення](class.ds-map.md)
- Встановлення значення за заданим ключем

# Ds\Map::put

(PECL ds \>= 1.0.0)

Ds\Map::put — Встановлення значення заданого ключа

### Опис

public
**Ds\Map::put**([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$key`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$value`): void

Зв'язує ключ `key` зі значенням `value`, якщо елемент із таким ключем
вже існує – його значення перезаписується.

> **Примітка**:
>
> Підтримуються значення типу об'єкта. Якщо об'єкт реалізує інтерфейс
> **Ds\Hashable**, перевірка здійснюється шляхом виклику методу об'єкта
> `equals`. Якщо об'єкт не реалізує інтерфейс **Ds\Hashable**, об'єкти
> повинні посилатися на той самий екземпляр класу.

> **Примітка**:
>
> Ви можете використовувати синтаксис масиву для доступу до значень, тобто.
> `$map["key"]`.

**Застереження**

Будьте обережні під час використання синтаксису масиву. Скалярні ключі
будуть приведені до цілого двигуна PHP. Наприклад, $map["1"]` буде
намагатися звернутися до `int(1)`, тоді як `$map->get("1")` звернеться до
правильний елемент.

Дивіться розділ [Массивы](language.types.array.md).

### Список параметрів

`key`
Ключ.

`value`
Значення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **Ds\Map::put()****

` <?php$map = new \Ds\Map();$map->put("a", 1);$map->put("b", 2);$map->put("c" , 3);print_r($map);?> `

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

**Приклад #2 Приклад використання **Ds\Map::put()** з об'єктами в
якість ключів**

` <?phpclass HashableObject implements \Ds\Hashable{    /**     * Значення, яке ми будемо використовувати в якості хеша. Не визначає ідентичність. */    private $value; public function __construct($value)    {        $this->value = $value; }    public function hash()    {        return $this->value; }    public function equals($obj): bool    {       return$$is->value ===$obj->value; }}$map = new \Ds\Map();$obj = new \ArrayIterator([]);// Використання одного і того ж екземпляра об'єкту декілька роз буде $$ , 1);$map->put($obj, 2);// Використання різних примірників одного і того ж класу буде створювати нові// елементи$map->put(new \stdClass(), >put(new \stdClass(), 4);// Використання однакових hashable-примірників кілька раз переписуватиме// попередні значення$map->put(new \HashableObject(1), 5);$ \HashableObject(1), 6);$map->put(new \HashableObject(2), 7);$map->put(new \HashableObject(2), 8);var_dump($map);?> `

Результатом виконання цього прикладу буде щось подібне:

object(Ds\Map)#1 (5) {
[0]=>
object(Ds\Pair)#7 (2) {
["key"]=>
object(ArrayIterator)#2 (1) {
["storage":"ArrayIterator":private]=>
array(0) {
}
}
["value"]=>
int(2)
}
[1]=>
object(Ds\Pair)#8 (2) {
["key"]=>
object(stdClass)#3 (0) {
}
["value"]=>
int(3)
}
[2]=>
object(Ds\Pair)#9 (2) {
["key"]=>
object(stdClass)#4 (0) {
}
["value"]=>
int(4)
}
[3]=>
object(Ds\Pair)#10 (2) {
["key"]=>
object(HashableObject)#5 (1) {
["value":"HashableObject":private]=>
int(1)
}
["value"]=>
int(6)
}
[4]=>
object(Ds\Pair)#11 (2) {
["key"]=>
object(HashableObject)#6 (1) {
["value":"HashableObject":private]=>
int(2)
}
["value"]=>
int(8)
}
}
