---
navigation:
  - worker.getstacked.md: '« Worker::getStacked'
  - worker.shutdown.md: 'Worker::shutdown »'
  - index.md: PHP Manual
  - class.worker.md: Worker
title: 'Worker::isShutdown'
---
# Worker::isShutdown

(PECL pthreads >= 2.0.0)

Worker::isShutdown — Визначення стану

### Опис

```methodsynopsis
public Worker::isShutdown(): bool
```

Визначає, чи зупинено Worker чи ні.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`** якщо зупинено і **`false`**, якщо ні.

### Приклади

**Приклад #1 Визначення стану**

```php
<?php
$worker = new Worker();
$worker->start();

var_dump($worker->isShutdown());

$worker->shutdown();

var_dump($worker->isShutdown());
```

Результат виконання цього прикладу:

```
bool(false)
bool(true)
```
