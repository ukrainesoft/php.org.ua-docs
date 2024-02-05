---
navigation:
  - ds-queue.count.md: '« Ds\\Queue::count'
  - ds-queue.jsonserialize.md: 'Ds\\Queue::jsonSerialize »'
  - index.md: PHP Manual
  - class.ds-queue.md: Ds\\Queue
title: 'Ds\\Queue::isEmpty'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Queue::isEmpty

(PECL ds >= 1.0.0)

Ds\\Queue::isEmpty — Перевіряє, чи порожня колекція

### Опис

```methodsynopsis
public Ds\Queue::isEmpty(): bool
```

Перевіряє, чи колекція порожня.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, если коллекция пуста,**`false`** в іншому випадку.

### Приклади

**Пример #1 Пример использования**Ds\\Queue::isEmpty()\*\*\*\*

```php
<?php
$a = new \Ds\Queue([1, 2, 3]);
$b = new \Ds\Queue();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(false)
bool(true)
```
