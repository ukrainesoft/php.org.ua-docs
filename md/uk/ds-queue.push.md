- [« Ds\Queue::pop](ds-queue.pop.md)
- [Ds\Queue::toArray »](ds-queue.toarray.md)

- [PHP Manual](index.md)
- [Черга](class.ds-queue.md)
- Додає значення у чергу

# Ds\Queue::push

(PECL ds \>= 1.0.0)

Ds\Queue::push — Додає значення в чергу

### Опис

public
**Ds\Queue::push**([mixed](language.types.declarations.md#language.types.declarations.mixed)
`...$values`): void

Додає значення `values` у чергу.

### Список параметрів

`values`
Значення, що додаються.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **Ds\Queue::push()****

` <?php$queue = new \Ds\Queue();$queue->push("a");$queue->push("b");$queue->push("c", "d" );$queue->push(...["e", "f"]);print_r($queue);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Queue Object
(
[0] => a
[1] => b
[2] => c
[3] => d
[4] => e
[5] => f
)
