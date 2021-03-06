- [« Ds\Sequence::sort](ds-sequence.sort.md)
- [Ds\Sequence::sum »](ds-sequence.sum.md)

- [PHP Manual](index.md)
- [Послідовність](class.ds-sequence.md)
- Повертає відсортовану за значенням копію колекції

# Ds\Sequence::sorted

(PECL ds \>= 1.0.0)

Ds\Sequence::sorted — Повертає відсортовану за значенням копію
колекції

### Опис

abstract public
**Ds\Sequence::sorted**([callable](language.types.callable.md)
`$comparator` = ?): [Ds\Sequence](class.ds-sequence.md)

Повертає відсортовану копію колекції, опціонально використовуючи
callback-функцію `comparator`.

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
*Не ціле* значення повернене з функції порівняння, такого як float,
буде приведено до цілого числа (int). Так що значення типу 0.99 та 0.1
будуть приведені до 0, що означатиме рівність порівнюваних значень.

### Значення, що повертаються

Повертає копію колекції, відсортовану за значенням.

### Приклади

**Приклад #1 Приклад використання **Ds\Sequence::sorted()****

` <?php$sequence = new \Ds\Vector([4, 5, 1, 3, 2]);print_r($sequence->sorted());?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Vector Object
(
[0] => 1
[1] => 2
[2] => 3
[3] => 4
[4] => 5
)

**Приклад #2 Приклад використання **Ds\Sequence::sorted()** з
callback-функцією порівняння**

` <?php$sequence = new \Ds\Vector([4, 5, 1, 3, 2]);$sorted = $sequence->sorted(function($a, $b) {    return $b <=> $a;});print_r($sorted);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Vector Object
(
[0] => 5
[1] => 4
[2] => 3
[3] => 2
[4] => 1
)
