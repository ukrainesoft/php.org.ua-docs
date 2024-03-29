---
navigation:
  - worker.shutdown.md: '« Worker::shutdown'
  - worker.unstack.md: 'Worker::unstack »'
  - index.md: PHP Manual
  - class.worker.md: Worker
title: 'Worker::stack'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Об'єкт типу [Threaded](class.threaded.md), який буде запущено Worker.

### Значення, що повертаються

Новий розмір стека.

### Приклади

**Приклад #1 Приміщення задачі на стек Worker для її запуску**

```php
<?php
$worker = new Worker();
$work = new class extends Threaded {};

var_dump($worker->stack($work));
```

Результат виконання наведеного прикладу:

```
int(1)
```
