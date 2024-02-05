---
navigation:
  - thread.join.md: '« Thread::join'
  - class.worker.md: Worker »
  - index.md: PHP Manual
  - class.thread.md: Thread
title: 'Thread::start'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Thread::start

(PECL pthreads >= 2.0.0)

Thread::start - Виконання

### Опис

```methodsynopsis
public Thread::start(int $options = ?): bool
```

Запуск нового потоку для виконання реалізованого методу запуску.

### Список параметрів

`options`

Необов'язкова маска констант успадкування за промовчанням PTHREADS\_INHERIT\_ALL.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Запуск потоку**

```php
<?php
class My extends Thread {
    public function run() {
        /** ... **/
    }
}
$my = new My();
var_dump($my->start());
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```
