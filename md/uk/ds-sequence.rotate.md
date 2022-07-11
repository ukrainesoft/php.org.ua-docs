- [« Ds\Sequence::reversed](ds-sequence.reversed.md)
- [Ds\Sequence::set »](ds-sequence.set.md)

- [PHP Manual](index.md)
- [Послідовність](class.ds-sequence.md)
- Перемотує послідовність на задану кількість значень

# Ds\Sequence::rotate

(PECL ds \>= 1.0.0)

Ds\Sequence::rotate — Перемотує послідовність на задане число
значень

### Опис

abstract public **Ds\Sequence::rotate**(int `$rotations`): void

Перемотує послідовність на задану кількість значень. Дана
операція аналогічна до виконання заданого кількість разів коду
`$sequence->push($sequence->shift())`, якщо кількість оборотів позитивна
і `$sequence->unshift($sequence->pop())`, якщо негативно.

### Список параметрів

`rotations`
Кількість значень, які треба "перемотати".

### Значення, що повертаються

Функція не повертає значення після виконання. Буде змінено поточну
послідовність.

### Приклади

**Приклад #1 Приклад використання **Ds\Sequence::rotate()****

` <?php$sequence = new \Ds\Vector(["a", "b", "c", "d"]);$sequence->rotate(1); // Аналогічно $a = $sequence->shift(); $sequence->push($a);print_r($sequence);$sequence->rotate(2);print_r($sequence);?> `

Результатом виконання цього прикладу буде щось подібне:

(
[0] => b
[1] => c
[2] => d
[3] => a
)
Ds\Vector Object
(
[0] => d
[1] => a
[2] => b
[3] => c
)
