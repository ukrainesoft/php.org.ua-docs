---
navigation:
  - ds-queue.capacity.md: '« Ds\\Queue::capacity'
  - ds-queue.construct.md: 'Ds\\Queue::\_\_construct »'
  - index.md: PHP Manual
  - class.ds-queue.md: Ds\\Queue
title: 'Ds\\Queue::clear'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Queue::clear

(PECL ds >= 1.0.0)

Ds\\Queue::clear — Видаляє всі значення

### Опис

```methodsynopsis
public Ds\Queue::clear(): void
```

Видаляє всі значення з черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**Ds\\Queue::clear()\*\*\*\*

```php
<?php
$queue = new \Ds\Queue([1, 2, 3]);
print_r($queue);

$queue->clear();
print_r($queue);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Queue Object
(
    [0] => 1
    [1] => 2
    [2] => 3
)
Ds\Queue Object
(
)
```
