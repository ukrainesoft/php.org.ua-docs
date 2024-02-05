---
navigation:
  - thread.getcreatorid.md: '« Thread::getCreatorId'
  - thread.getcurrentthreadid.md: 'Thread::getCurrentThreadId »'
  - index.md: PHP Manual
  - class.thread.md: Thread
title: 'Thread::getCurrentThread'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Thread::getCurrentThread

(PECL pthreads >= 2.0.0)

Thread::getCurrentThread — Ідентифікація

### Опис

```methodsynopsis
public static Thread::getCurrentThread(): Thread
```

Повертає посилання на поточний потік, що виконується.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт, що представляє поточний потік, що виконується.

### Приклади

**Приклад #1 Повертає посилання на поточний потік, що виконується.**

```php
<?php
class My extends Thread {
    public function run() {
        var_dump(Thread::getCurrentThread());
    }
}
$my = new My();
$my->start();
?>
```

Результат виконання наведеного прикладу:

```
object(My)#2 (0) {
}
```
