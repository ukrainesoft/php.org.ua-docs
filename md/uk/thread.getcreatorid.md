---
navigation:
  - class.thread.md: « Thread
  - thread.getcurrentthread.md: 'Thread::getCurrentThread »'
  - index.md: PHP Manual
  - class.thread.md: Thread
title: 'Thread::getCreatorId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Thread::getCreatorId

(PECL pthreads >= 2.0.0)

Thread::getCreatorId - Ідентифікація

### Опис

```methodsynopsis
public Thread::getCreatorId(): int
```

Повертає ідентифікатор потоку, який створив цей потік.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Числовий ідентифікатор.

### Приклади

**Приклад #1 Повертає ідентифікатор потоку, який створив цей потік**

```php
<?php
class My extends Thread {
    public function run() {
        printf("%s создан потоком #%lu\n", __CLASS__, $this->getCreatorId());
    }
}
$my = new My();
$my->start();
?>
```

Результат виконання наведеного прикладу:

```
My создан потоком #123456778899
```
