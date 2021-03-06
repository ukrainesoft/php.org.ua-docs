- [« Ds\Deque::reverse](ds-deque.reverse.md)
- [Ds\Deque::rotate »](ds-deque.rotate.md)

- [PHP Manual](index.md)
- [Двостороння черга](class.ds-deque.md)
- Повертає перегорнуту копію двосторонньої черги

# Ds\Deque::reversed

(PECL ds \>= 1.0.0)

Ds\Deque::reversed — Повертає перегорнуту копію двосторонньої черги

### Опис

public **Ds\Deque::reversed**(): [Ds\Deque](class.ds-deque.md)

Повертає перегорнуту копію двосторонньої черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перегорнута копія двосторонньої черги.

> **Примітка**:
>
> Поточна двостороння черга не зміниться.

### Приклади

**Приклад #1 Приклад використання **Ds\Deque::reversed()****

` <?php$deque = new \Ds\Deque(["a", "b", "c"]);print_r($deque->reversed());print_r($deque);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Deque Object
(
[0] => c
[1] => b
[2] => a
)
Ds\Deque Object
(
[0] => a
[1] => b
[2] => c
)
