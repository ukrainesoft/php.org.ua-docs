---
navigation:
  - ds-queue.count.md: '« DsQueue::count'
  - ds-queue.jsonserialize.md: 'ДсQueue::jsonSerialize »'
  - index.md: PHP Manual
  - class.ds-queue.md: Черга
title: 'ДсQueue::isEmpty'
---
# ДсQueue::isEmpty

(PECL ds >= 1.0.0)

ДсQueue::isEmpty — Перевіряє, чи порожня колекція

### Опис

```methodsynopsis
public Ds\Queue::isEmpty(): bool
```

Перевіряє, чи колекція порожня.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо колекція порожня, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ДсQueue::isEmpty()****

```php
<?php
$a = new \Ds\Queue([1, 2, 3]);
$b = new \Ds\Queue();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(false)
bool(true)
```
