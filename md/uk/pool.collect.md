---
navigation:
  - class.pool.md: « Pool
  - pool.construct.md: 'Pool::\_\_construct »'
  - index.md: PHP Manual
  - class.pool.md: Pool
title: 'Pool::collect'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Pool::collect

(PECL pthreads >= 2.0.0)

Pool::collect — Збирає посилання на виконані завдання

### Опис

```methodsynopsis
public Pool::collect(Callable $collector = ?): int
```

Дозволяє пулу збирати посилання, визначені як сміття додатковим збирачем.

### Список параметрів

`collector`

Callback - функція збирача, яка повертає логічне значення, що вказує, чи може бути завдання зібрано чи ні. Тільки в окремих випадках може знадобитися спеціальний збирач.

### Значення, що повертаються

Кількість завдань, що залишилися в пулі, які потрібно зібрати.

### список змін

| Версия | Опис |
| --- | --- |
| v3 | Тепер повертається ціле число, а параметр `collector` тепер необов'язковий. |

### Приклади

**Приклад #1 Простий приклад використання **Pool::collect()****

```php
<?php
$pool = new Pool(4);

for ($i = 0; $i < 15; ++$i) {
    $pool->submit(new class extends Threaded {});
}

while ($pool->collect()); // до тех пор, пока все задачи не закончат выполнение

$pool->shutdown();
```
