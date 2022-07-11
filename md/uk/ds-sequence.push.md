- [« Ds\Sequence::pop](ds-sequence.pop.md)
- [Ds\Sequence::reduce »](ds-sequence.reduce.md)

- [PHP Manual](index.md)
- [Послідовність](class.ds-sequence.md)
- Додає значення до кінця послідовності

# Ds\Sequence::push

(PECL ds \>= 1.0.0)

Ds\Sequence::push — Додає значення до кінця послідовності

### Опис

abstract public
**Ds\Sequence::push**([mixed](language.types.declarations.md#language.types.declarations.mixed)
`...$values`): void

Додає значення до кінця послідовності.

### Список параметрів

`values`
Значення, що додаються.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **Ds\Sequence::push()****

` <?php$sequence = new \Ds\Vector();$sequence->push("a");$sequence->push("b");$sequence->push("c", "d" );$sequence->push(...["e", "f"]);print_r($sequence);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Vector Object
(
[0] => a
[1] => b
[2] => c
[3] => d
[4] => e
[5] => f
)
