- [« Worker::shutdown](worker.shutdown.md)
- [Worker::unstack »](worker.unstack.md)

- [PHP Manual](index.md)
- [Worker](class.worker.md)
- Покласти завдання на стек

# Worker::stack

(PECL pthreads \>= 2.0.0)

Worker::stack — Покласти завдання на стек

### Опис

public **Worker::stack**([Threaded](class.threaded.md) `&$work`): int

Додає завдання на стек заданому Worker.

### Список параметрів

`work`
Об'єкт типу [Threaded](class.threaded.md), який буде запущено
Worker.

### Значення, що повертаються

Новий розмір стека.

### Приклади

**Приклад #1 Приміщення задачі на стек Worker для її запуску**

` <?php$worker = new Worker();$work = new class extends Threaded {};var_dump($worker->stack($work)); `

Результат виконання цього прикладу:

int(1)
