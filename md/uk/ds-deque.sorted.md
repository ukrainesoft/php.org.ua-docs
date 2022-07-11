- [« Ds\Deque::sort](ds-deque.sort.md)
- [Ds\Deque::sum »](ds-deque.sum.md)

- [PHP Manual](index.md)
- [Двостороння черга](class.ds-deque.md)
- Повертає відсортовану за значенням копію двосторонньої черги

# Ds\Deque::sorted

(PECL ds \>= 1.0.0)

Ds\Deque::sorted — Повертає відсортовану за значенням копію
двосторонньої черги

### Опис

public **Ds\Deque::sorted**([callable](language.types.callable.md)
`$comparator` = ?): [Ds\Deque](class.ds-deque.md)

Повертає відсортовану копію двосторонньої черги, опціонально
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

Повертає відсортовану за значенням копію двосторонньої черги.

### Приклади

**Приклад #1 Приклад використання **Ds\Deque::sorted()****

` <?php$deque = new \Ds\Deque([4, 5, 1, 3, 2]);print_r($deque->sorted());?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Deque Object
(
[0] => 1
[1] => 2
[2] => 3
[3] => 4
[4] => 5
)

**Приклад #2 Приклад використання **Ds\Deque::sorted()** з
callback-функцією порівняння**

` <?php$deque = new \Ds\Deque([4, 5, 1, 3, 2]);$sorted = $deque->sorted(function($a, $b) {    return $b <=> $a;});print_r($sorted);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Deque Object
(
[0] => 5
[1] => 4
[2] => 3
[3] => 2
[4] => 1
)
