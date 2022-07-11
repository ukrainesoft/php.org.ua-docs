- [« Ds\Vector::reversed](ds-vector.reversed.md)
- [Ds\Vector::set »](ds-vector.set.md)

- [PHP Manual](index.md)
- [Вектор](class.ds-vector.md)
- Перемотує вектор на задану кількість значень

# Ds\Vector::rotate

(PECL ds \>= 1.0.0)

Ds\Vector::rotate — Перемотує вектор на задану кількість значень

### Опис

public **Ds\Vector::rotate**(int `$rotations`): void

Перемотує вектор на задану кількість значень. Ця операція
аналогічна до виконання задану кількість разів коду
`$vector->push($vector->shift())`, якщо кількість оборотів позитивна і
`$vector->unshift($vector->pop())`, якщо негативно.

### Список параметрів

`rotations`
Кількість значень, які треба "перемотати".

### Значення, що повертаються

Функція не повертає значення після виконання. Буде змінено поточний
вектор.

### Приклади

**Приклад #1 Приклад використання **Ds\Vector::rotate()****

` <?php$vector = new \Ds\Vector(["a", "b", "c", "d"]);$vector->rotate(1); // Аналогічно $a = $vector->shift(); $vector->push($a);print_r($vector);$vector->rotate(2);print_r($vector);?> `

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
