---
navigation:
  - worker.isshutdown.md: '« Worker::isShutdown'
  - worker.stack.md: 'Worker::stack »'
  - index.md: PHP Manual
  - class.worker.md: Worker
title: 'Worker::shutdown'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Worker::shutdown

(PECL pthreads >= 2.0.0)

Worker::shutdown — Зупинити Worker

### Опис

```methodsynopsis
public Worker::shutdown(): bool
```

Зупинити Worker після запуску всіх завдань зі стека.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Зупинка Worker**

```php
<?php
$my = new Worker();
$my->start();
/* stack/execute tasks */
var_dump($my->shutdown());
```

Результат виконання наведеного прикладу:

```
bool(true)
```
