---
navigation:
  - thread.isrunning.md: '« Threaded::isRunning'
  - threaded.merge.md: 'Threaded::merge »'
  - index.md: PHP Manual
  - class.threaded.md: Threaded
title: 'Threaded::isTerminated'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Threaded::isTerminated

(PECL pthreads >= 2.0.0)

Threaded::isTerminated — Визначення стану

### Опис

```methodsynopsis
public Threaded::isTerminated(): bool
```

Повідомляє, чи об'єкт, на який вказує посилання, припинено під час виконання; чи відбулися фатальні помилки, чи були викинуті неперехоплені винятки.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Логічне значення стану об'єкта.

### Приклади

**Приклад #1 Визначення стану вказаного об'єкта**

```php
<?php
class My extends Thread {
    public function run() {
        i_do_not_exist();
    }
}
$my = new My();
$my->start();
$my->join();
var_dump($my->isTerminated());
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```
