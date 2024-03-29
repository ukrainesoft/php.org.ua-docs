---
navigation:
  - pool.submit.md: '« Pool::submit'
  - class.volatile.md: Volatile »
  - index.md: PHP Manual
  - class.pool.md: Pool
title: 'Pool::submitTo'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Pool::submitTo

(PECL pthreads >= 2.0.0)

Pool::submitTo — Відправляє завдання конкретному воркер для виконання

### Опис

```methodsynopsis
public Pool::submitTo(int $worker, Threaded $task): int
```

Відправляє завдання вказаному воркеру в пулі. Воркери індексуються з 0 і будуть існувати тільки в тому випадку, якщо пулу необхідно їх створити (оскільки потоки створюються ліниво).

### Список параметрів

`worker`

Воркер, до якого потрібно додати завдання, починаючи з

`task`

Завдання для виконання

### Значення, що повертаються

Ідентифікатор воркера, який прийняв завдання.

### Приклади

**Приклад #1 Надсилання завдань конкретному воркеру**

```php
<?php
class Task extends Threaded {
    public function run() {
        var_dump(Thread::getCurrentThreadID());
    }
}

$pool = new Pool(2);

$pool->submit(new Task());

for ($i = 0; $i < 5; ++$i) {
    $pool->submitTo(0, new Task()); // добавление всех заданий первому воркеру
}

$pool->submitTo(1, new Task()); // не может добавить задачу второму воркеру, потому что его ещё не существует

$pool->shutdown();
```

Результат виконання наведеного прикладу:

```
int(4475011072)
int(4475011072)
int(4475011072)
int(4475011072)
int(4475011072)
int(4475011072)

Fatal error: Uncaught Exception: The selected worker (1) does not exist in %s:%d
```
