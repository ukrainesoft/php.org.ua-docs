---
navigation:
  - pool.collect.md: '« Pool::collect'
  - pool.resize.md: 'Pool::resize »'
  - index.md: PHP Manual
  - class.pool.md: Pool
title: 'Pool::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Pool::\_\_construct

(PECL pthreads >= 2.0.0)

Pool::\_\_construct - Створює новий пул воркерів

### Опис

public**Pool::\_\_construct**(int`$size`, string`$class`\= ?, array`$ctor`

Створює новий пул робітників. Пули ліниво створюють свої потоки, що означає, що нові потоки будуть створюватися тільки тоді, коли вони необхідні виконання завдань.

### Список параметрів

`size`

Максимальна кількість воркерів, яка може створити цей пул

`class`

Клас для нових воркерів. Якщо клас не вказано, то за умовчанням використовується клас [Worker](class.worker.md)

`ctor`

Масив аргументів передачі конструкторам нових воркерам.

### Приклади

**Приклад #1 Створення пулів**

```php
<?php
class MyWorker extends Worker {

    public function __construct(Something $something) {
        $this->something = $something;
    }

    public function run() {
        /** ... **/
    }
}

$pool = new Pool(8, \MyWorker::class, [new Something()]);

var_dump($pool);
?>
```

Результат виконання наведеного прикладу:

```
object(Pool)#1 (6) {
  ["size":protected]=>
  int(8)
  ["class":protected]=>
  string(8) "MyWorker"
  ["workers":protected]=>
  NULL
  ["work":protected]=>
  NULL
  ["ctor":protected]=>
  array(1) {
    [0]=>
    object(Something)#2 (0) {
    }
  }
  ["last":protected]=>
  int(0)
}
```
