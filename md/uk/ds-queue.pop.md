---
navigation:
  - ds-queue.peek.md: '« Ds\\Queue::peek'
  - ds-queue.push.md: 'Ds\\Queue::push »'
  - index.md: PHP Manual
  - class.ds-queue.md: Ds\\Queue
title: 'Ds\\Queue::pop'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Queue::pop

(PECL ds >= 1.0.0)

Ds\\Queue::pop — Видаляє та повертає значення з початку черги

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

**Приклад #1 Приклад використання** Ds\\Queue::pop()\*\*\*\*

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

Висновок наведеного прикладу буде схожим на:

```
string(1) "a"
string(1) "b"
string(1) "c"
```
