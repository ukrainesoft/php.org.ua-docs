- [« Ds\Deque::get](ds-deque.get.md)
- [Ds\Deque::isEmpty »](ds-deque.isempty.md)

- [PHP Manual](index.md)
- [Двостороння черга](class.ds-deque.md)
- Вставляє значення за вказаним індексом

# Ds\Deque::insert

(PECL ds \>= 1.0.0)

Ds\Deque::insert — Вставляє значення за вказаним індексом

### Опис

public **Ds\Deque::insert**(int `$index`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`...$values`): void

Вставляє значення за вказаним індексом.

### Список параметрів

`index`
Індекс, яким необхідно здійснити вставку.
`0 <= index <= count`

> **Примітка**:
>
> Можна вказувати індекс, що дорівнює кількості елементів двосторонньої
> черги.

`values`
Значення чи значення для вставки.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток
[OutOfRangeException](class.outofrangeexception.md) у разі
некоректного індексу.

### Приклади

**Приклад #1 Приклад використання **Ds\Deque::insert()****

` <?php$deque = new \Ds\Deque();$deque->insert(0, "e"); // [e]$deque->insert(1, "f"); // [e, f]$deque->insert(2, "g"); // [e, f, g]$deque->insert(0, "a", "b"); // [a, b, e, f, g]$deque->insert(2, ...["c", "d"]); // [a, b, c, d, e, f, g]var_dump($deque);?> `

Результатом виконання цього прикладу буде щось подібне:

object(Ds\Deque)#1 (7) {
[0]=>
string(1) "a"
[1]=>
string(1) "b"
[2]=>
string(1) "c"
[3]=>
string(1) "d"
[4]=>
string(1) "e"
[5]=>
string(1) "f"
[6]=>
string(1) "g"
}
