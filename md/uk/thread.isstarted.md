---
navigation:
  - thread.isjoined.md: '« Thread::isJoined'
  - thread.join.md: 'Thread::join »'
  - index.md: PHP Manual
  - class.thread.md: Thread
title: 'Thread::isStarted'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Thread::isStarted

(PECL pthreads >= 2.0.0)

Thread::isStarted — Визначення стану

### Опис

```methodsynopsis
public Thread::isStarted(): bool
```

Повідомляє, чи було запущено вказаний потік.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Повідомляє, чи було запущено зазначений потік**

```php
<?php
$worker = new Worker();
$worker->start();
var_dump($worker->isStarted());
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```
