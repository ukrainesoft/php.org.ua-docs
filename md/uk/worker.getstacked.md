---
navigation:
  - worker.collect.md: '« Worker::collect'
  - worker.isshutdown.md: 'Worker::isShutdown »'
  - index.md: PHP Manual
  - class.worker.md: Worker
title: 'Worker::getStacked'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Worker::getStacked

(PECL pthreads >= 2.0.0)

Worker::getStacked — Повертає поточний розмір стека

### Опис

```methodsynopsis
public Worker::getStacked(): int
```

Повертає кількість завдань, що залишилися у стеку.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість завдань, що залишилися в стеку і чекають на запуск.

### Приклади

**Пример #1 Пример использования**Worker::getStacked\*\*\*\*

```php
<?php
$worker = new Worker();

for ($i = 0; $i < 5; ++$i) {
    $worker->stack(new class extends Threaded {});
}

echo "There are {$worker->getStacked()} stacked tasks\n";
```

Результат виконання наведеного прикладу:

```
There are 5 stacked tasks
```
