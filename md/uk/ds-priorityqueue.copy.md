- [« Ds\PriorityQueue::\_\_construct](ds-priorityqueue.construct.md)
- [Ds\PriorityQueue::count »](ds-priorityqueue.count.md)

- [PHP Manual](index.md)
- [Черга з пріоритетом](class.ds-priorityqueue.md)
- Повертає поверхневу копію черги

# Ds\PriorityQueue::copy

(PECL ds \>= 1.0.0)

Ds\PriorityQueue::copy — Повертає поверхневу копію черги

### Опис

public **Ds\PriorityQueue::copy**():
[Ds\PriorityQueue](class.ds-priorityqueue.md)

Повертає поверхневу копію черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поверхнева копія черги.

### Приклади

**Приклад #1 Приклад використання **Ds\PriorityQueue::copy()****

` <?php$queue = new \Ds\PriorityQueue();$queue->push("a",  5);$queue->push("b", 15);$queue->push("c" , 10);print_r($queue->copy());?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\PriorityQueue Object
(
[0] => b
[1] => c
[2] => a
)
