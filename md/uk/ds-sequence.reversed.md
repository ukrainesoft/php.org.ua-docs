- [« Ds\Sequence::reverse](ds-sequence.reverse.md)
- [Ds\Sequence::rotate »](ds-sequence.rotate.md)

- [PHP Manual](index.md)
- [Послідовність](class.ds-sequence.md)
- Повертає перегорнуту копію колекції

# Ds\Sequence::reversed

(PECL ds \>= 1.0.0)

Ds\Sequence::reversed — Повертає перегорнуту копію колекції

### Опис

abstract public **Ds\Sequence::reversed**():
[Ds\Sequence](class.ds-sequence.md)

Повертає копію колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перегорнута копія колекції.

> **Примітка**:
>
> Поточна колекція не зміниться.

### Приклади

**Приклад #1 Приклад використання **Ds\Sequence::reversed()****

` <?php$sequence = new \Ds\Vector(["a", "b", "c"]);print_r($sequence->reversed());print_r($sequence);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Vector Object
(
[0] => c
[1] => b
[2] => a
)
Ds\Vector Object
(
[0] => a
[1] => b
[2] => c
)
