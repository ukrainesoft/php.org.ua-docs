- [« Ds\Vector::slice](ds-vector.slice.md)
- [Ds\Vector::sorted »](ds-vector.sorted.md)

- [PHP Manual](index.md)
- [Вектор](class.ds-vector.md)
- Сортує вектор

# Ds\Vector::sort

(PECL ds \>= 1.0.0)

Ds\Vector::sort — Сортує вектор

### Опис

public **Ds\Vector::sort**([callable](language.types.callable.md)
`$comparator` = ?): void

Сортує вектор, опціонально використовуючи callback-функцію `comparator`.

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

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **Ds\Vector::sort()****

` <?php$vector = new \Ds\Vector([4, 5, 1, 3, 2]);$vector->sort();print_r($vector);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Vector Object
(
[0] => 1
[1] => 2
[2] => 3
[3] => 4
[4] => 5
)

**Приклад #2 Приклад використання **Ds\Vector::sort()** з
callback-функцією порівняння**

` <?php$vector = new \Ds\Vector([4, 5, 1, 3, 2]);$vector->sort(function($a, $b) {   return $b <=> $a; });print_r($vector);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Vector Object
(
[0] => 5
[1] => 4
[2] => 3
[3] => 2
[4] => 1
)
