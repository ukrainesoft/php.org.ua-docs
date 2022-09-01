---
navigation:
  - thread.getcreatorid.html: '« Thread::getCreatorId'
  - thread.getcurrentthreadid.html: 'Thread::getCurrentThreadId »'
  - index.html: PHP Manual
  - class.thread.html: Thread
title: 'Thread::getCurrentThread'
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
class My extends Thread {
    public function run() {
        var_dump(Thread::getCurrentThread());
    }
}
$my = new My();
$my->start();
?>
```

Результат виконання цього прикладу:

```
object(My)#2 (0) {
}
```
