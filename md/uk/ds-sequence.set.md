- [« Ds\Sequence::rotate](ds-sequence.rotate.md)
- [Ds\Sequence::shift »](ds-sequence.shift.md)

- [PHP Manual](index.md)
- [Послідовність](class.ds-sequence.md)
- Замінює значення за вказаним індексом

# Ds\Sequence::set

(PECL ds \>= 1.0.0)

Ds\Sequence::set — Замінює значення за вказаним індексом

### Опис

abstract public **Ds\Sequence::set**(int `$index`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$value`): void

Замінює значення за вказаним індексом.

### Список параметрів

`index`
Індекс, яким треба замінити значення.

`value`
Нове значення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток
[OutOfRangeException](class.outofrangeexception.md), якщо індекс
некоректний.

### Приклади

**Приклад #1 Приклад використання **Ds\Sequence::set()****

` <?php$sequence = new \Ds\Vector(["a", "b", "c"]);$sequence->set(1, "_");print_r($sequence);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Vector Object
(
[0] => a
[1] => _
[2] => c
)

**Приклад #2 Приклад використання **Ds\Sequence::set()** з синтаксисом
масиву**

` <?php$sequence = new \Ds\Vector(["a", "b", "c"]);$sequence[1] = "_";print_r($sequence);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Vector Object
(
[0] => a
[1] => _
[2] => c
)
