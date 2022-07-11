- [« Ds\Sequence::remove](ds-sequence.remove.md)
- [Ds\Sequence::reversed »](ds-sequence.reversed.md)

- [PHP Manual](index.md)
- [Послідовність](class.ds-sequence.md)
- Перевертає поточну колекцію

# Ds\Sequence::reverse

(PECL ds \>= 1.0.0)

Ds\Sequence::reverse — Перевертає поточну колекцію

### Опис

abstract public **Ds\Sequence::reverse**(): void

Перевертає поточну колекцію.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **Ds\Sequence::reverse()****

` <?php$sequence = new \Ds\Vector(["a", "b", "c"]);$sequence->reverse();print_r($sequence);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Vector Object
(
[0] => c
[1] => b
[2] => a
)
