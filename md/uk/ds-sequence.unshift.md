- [« Ds\Sequence::sum](ds-sequence.sum.md)
- [Вектор »](class.ds-vector.md)

- [PHP Manual](index.md)
- [Послідовність](class.ds-sequence.md)
- Додає значення на початок послідовності

# Ds\Sequence::unshift

(PECL ds \>= 1.0.0)

Ds\Sequence::unshift — Додає значення на початок послідовності

### Опис

abstract public
**Ds\Sequence::unshift**([mixed](language.types.declarations.md#language.types.declarations.mixed)
$values = ?): void

Додає значення на початок послідовності, переміщуючи всі поточні
значення вперед, щоб звільнити місце для нових значень.

### Список параметрів

`values`
Значення, що додаються.

> **Примітка**:
>
> Багато значень додаються в тому порядку, як вони були передані.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **Ds\Sequence::unshift()****

` <?php$sequence = new \Ds\Vector([1, 2, 3]);$sequence->unshift("a");$sequence->unshift("b", "c");print_r( $ sequence);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Vector Object
(
[0] => b
[1] => c
[2] => a
[3] => 1
[4] => 2
[5] => 3
)
