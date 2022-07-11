- [« Ds\Deque::capacity](ds-deque.capacity.md)
- [Ds\Deque::\_\_construct »](ds-deque.construct.md)

- [PHP Manual](index.md)
- [Двостороння черга](class.ds-deque.md)
- Видаляє всі значення з двосторонньої черги

# Ds\Deque::clear

(PECL ds \>= 1.0.0)

Ds\Deque::clear — Видалення всіх значень із двосторонньої черги

### Опис

public **Ds\Deque::clear**(): void

Видаляє всі значення двосторонньої черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **Ds\Deque::clear()****

` <?php$deque = new \Ds\Deque([1, 2, 3]);print_r($deque);$deque->clear();print_r($deque);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Deque Object
(
[0] => 1
[1] => 2
[2] => 3
)
Ds\Deque Object
(
)
