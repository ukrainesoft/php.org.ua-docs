---
navigation:
  - worker.stack.md: '« Worker::stack'
  - class.collectable.md: Collectable »
  - index.md: PHP Manual
  - class.worker.md: Worker
title: 'Worker::unstack'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Worker::unstack

(PECL pthreads >= 2.0.0)

Worker::unstack — Прибрати завдання зі стека

### Опис

```methodsynopsis
public Worker::unstack(): int
```

Прибирає перше завдання (найстарішу) зі стека.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Новий розмір стека.

### список змін

| Версия | Опис |
| --- | --- |
| v3 | Прибрано параметр, у якому вказувалося завдання видалення. Тепер завжди видаляється перше завдання. |

### Приклади

**Приклад #1 Видалення об'єктів зі стека Worker**

```php
<?php
$my = new Worker();
$work = new class extends Threaded {};

var_dump($my->stack($work));
var_dump($my->unstack());
```

Результат виконання наведеного прикладу:

```
int(1)
int(0)
```
