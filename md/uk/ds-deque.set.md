- [« Ds\Deque::rotate](ds-deque.rotate.md)
- [Ds\Deque::shift »](ds-deque.shift.md)

- [PHP Manual](index.md)
- [Двостороння черга](class.ds-deque.md)
- Замінює значення за вказаним індексом

# Ds\Deque::set

(PECL ds \>= 1.0.0)

Ds\Deque::set — Замінює значення за вказаним індексом

### Опис

public **Ds\Deque::set**(int `$index`,
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

**Приклад #1 Приклад використання **Ds\Deque::set()****

` <?php$deque = new \Ds\Deque(["a", "b", "c"]);$deque->set(1, "_");print_r($deque);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Deque Object
(
[0] => a
[1] => _
[2] => c
)

**Приклад #2 Приклад використання **Ds\Deque::set()** із синтаксисом
масиву**

` <?php$deque = new \Ds\Deque(["a", "b", "c"]);$deque[1] = "_";print_r($deque);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Deque Object
(
[0] => a
[1] => _
[2] => c
)
