---
navigation:
  - thread.isjoined.md: '« Thread::isJoined'
  - thread.join.md: 'Thread::join »'
  - index.md: PHP Manual
  - class.thread.md: Thread
title: 'Thread::isStarted'
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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Повідомляє, чи було запущено зазначений потік**

```php
<?php
$worker = new Worker();
$worker->start();
var_dump($worker->isStarted());
?>
```

Результат виконання цього прикладу:

```
bool(true)
```
