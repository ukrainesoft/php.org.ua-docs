- [« Ds\Deque::contains](ds-deque.contains.md)
- [Ds\Deque::count »](ds-deque.count.md)

- [PHP Manual](index.md)
- [Двостороння черга](class.ds-deque.md)
- Повертає поверхневу копію колекції

# Ds\Deque::copy

(PECL ds \>= 1.0.0)

Ds\Deque::copy — Повертає поверхневу копію колекції

### Опис

public **Ds\Deque::copy**(): [Ds\Deque](class.ds-deque.md)

Повертає поверхневу копію двосторонньої черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поверхнева копія двосторонньої черги.

### Приклади

**Приклад #1 Приклад використання **Ds\Deque::copy()****

` <?php$a = new \Ds\Deque([1, 2, 3]);$b = $a->copy();$b->push(4);print_r($a);print_r( $b);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Deque Object
(
[0] => 1
[1] => 2
[2] => 3
)
Ds\Deque Object
(
[0] => 1
[1] => 2
[2] => 3
[3] => 4
)
