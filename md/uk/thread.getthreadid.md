---
navigation:
  - thread.getcurrentthreadid.md: '« Thread::getCurrentThreadId'
  - thread.isjoined.md: 'Thread::isJoined »'
  - index.md: PHP Manual
  - class.thread.md: Thread
title: 'Thread::getThreadId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Thread::getThreadId

(PECL pthreads >= 2.0.0)

Thread::getThreadId - Ідентифікація

### Опис

```methodsynopsis
public Thread::getThreadId(): int
```

Повертає ідентифікатор вказаного потоку

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Числовий ідентифікатор.

### Приклади

**Приклад #1 Повертає ідентифікатор вказаного потоку**

```php
<?php
class My extends Thread {
    public function run() {
        printf("%s является потоком #%lu\n", __CLASS__, $this->getThreadId());
    }
}
$my = new My();
$my->start();
?>
```

Результат виконання наведеного прикладу:

```
My является потоком #123456778899
```
