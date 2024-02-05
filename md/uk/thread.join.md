---
navigation:
  - thread.isstarted.md: '« Thread::isStarted'
  - thread.start.md: 'Thread::start »'
  - index.md: PHP Manual
  - class.thread.md: Thread
title: 'Thread::join'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Thread::join

(PECL pthreads >= 2.0.0)

Thread::join — Синхронізація

### Опис

```methodsynopsis
public Thread::join(): bool
```

Примушує викликаючий контекст чекати, поки вказаний потік завершить виконання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приєднання до зазначеного процесу**

```php
<?php
class My extends Thread {
    public function run() {
        /* ... */
    }
}
$my = new My();
$my->start();
/* ... */
var_dump($my->join());
/* ... */
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```
