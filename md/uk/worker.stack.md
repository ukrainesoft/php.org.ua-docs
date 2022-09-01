---
navigation:
  - worker.shutdown.html: '« Worker::shutdown'
  - worker.unstack.html: 'Worker::unstack »'
  - index.html: PHP Manual
  - class.worker.html: Worker
title: 'Worker::stack'
---
# Worker::stack

(PECL pthreads >= 2.0.0)

Worker::stack — Покласти завдання на стек

### Опис

```methodsynopsis
public Worker::stack(Threaded &$work): int
```

Додає завдання на стек заданому Worker.

### Список параметрів

`work`

Об'єкт типу [Threaded](class.threaded.html), який буде запущено Worker.

### Значення, що повертаються

Новий розмір стека.

### Приклади

**Приклад #1 Приміщення задачі на стек Worker для її запуску**

```php
<?php
$worker = new Worker();
$work = new class extends Threaded {};

var_dump($worker->stack($work));
```

Результат виконання цього прикладу:

```
int(1)
```
