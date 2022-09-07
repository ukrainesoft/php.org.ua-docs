---
navigation:
  - ds-queue.peek.md: '« DsQueue::peek'
  - ds-queue.push.md: 'ДсQueue::push »'
  - index.md: PHP Manual
  - class.ds-queue.md: Черга
title: 'ДсQueue::pop'
---
# ДсQueue::pop

(PECL ds >= 1.0.0)

ДсQueue::pop — Видаляє та повертає значення з початку черги

### Опис

```methodsynopsis
public Ds\Queue::pop(): mixed
```

Видаляє та повертає значення з початку черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Видалене значення з початку черги.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо колекція порожня.

### Приклади

**Приклад #1 Приклад використання **ДсQueue::pop()****

```php
<?php
$queue = new \Ds\Queue();

$queue->push("a");
$queue->push("b");
$queue->push("c");

var_dump($queue->pop());
var_dump($queue->pop());
var_dump($queue->pop());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "a"
string(1) "b"
string(1) "c"
```
