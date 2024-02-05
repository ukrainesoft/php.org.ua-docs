---
navigation:
  - class.worker.md: « Worker
  - worker.getstacked.md: 'Worker::getStacked »'
  - index.md: PHP Manual
  - class.worker.md: Worker
title: 'Worker::collect'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Worker::collect

(PECL pthreads >= 3.0.0)

Worker::collect — Зібрати посилання на завершені завдання

### Опис

```methodsynopsis
public Worker::collect(Callable $collector = ?): int
```

Дозволяє Worker зібрати "сміттєві" посилання на завдання. Опціонально можна задати користувальницький збирач.

### Список параметрів

`collector`

Складальник типу Callable, який має повертати **`true`** або **`false`** залежно від цього, чи можна зібрати завдання. Випадки, коли вам може знадобитися власний збирач, дуже рідкісні.

### Значення, що повертаються

Кількість завдань, що залишилися в стеку Worker, які будуть зібрані.

### Приклади

**Приклад #1 Приклад використання** Worker::collect()\*\*\*\*

```php
<?php
$worker = new Worker();

echo "Сейчас на стеке {$worker->collect()} задач, которые нужно собрать\n";

for ($i = 0; $i < 15; ++$i) {
    $worker->stack(new class extends Threaded {});
}

echo "На стеке {$worker->collect()} задач, которые нужно собрать\n";

$worker->start();

while ($worker->collect()); // ждём, пока все задачи не завершат исполнение

echo "Теперь на стеке {$worker->collect()} задач, ждущих, когда их соберут\n";

$worker->shutdown();
```

Результат виконання наведеного прикладу:

```
Сейчас на стеке 0 задач, которые нужно собрать
На стеке 15 задач, которые нужно собрать
Теперь на стеке 0 задач, ждущих, когда их соберут
```
