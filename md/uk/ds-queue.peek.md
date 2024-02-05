---
navigation:
  - ds-queue.jsonserialize.md: '« Ds\\Queue::jsonSerialize'
  - ds-queue.pop.md: 'Ds\\Queue::pop »'
  - index.md: PHP Manual
  - class.ds-queue.md: Ds\\Queue
title: 'Ds\\Queue::peek'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Queue::peek

(PECL ds >= 1.0.0)

Ds\\Queue::peek — Повертає значення з початку черги

### Опис

```methodsynopsis
public Ds\Queue::peek(): mixed
```

Повертає значення із початку черги, але не видаляє його.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Значення із початку черги.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо колекція порожня.

### Приклади

**Приклад #1 Приклад використання** Ds\\Queue::peek()\*\*\*\*

```php
<?php
$queue = new \Ds\Queue();

$queue->push("a");
$queue->push("b");
$queue->push("c");

var_dump($queue->peek());
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(1) "a"
```
