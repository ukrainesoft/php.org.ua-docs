---
navigation:
  - ds-queue.pop.md: '« Ds\\Queue::pop'
  - ds-queue.toarray.md: 'Ds\\Queue::toArray »'
  - index.md: PHP Manual
  - class.ds-queue.md: Ds\\Queue
title: 'Ds\\Queue::push'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Queue::push

(PECL ds >= 1.0.0)

Ds\\Queue::push — Додає значення в чергу

### Опис

```methodsynopsis
public Ds\Queue::push(mixed ...$values): void
```

Добавляет значения`values` в чергу.

### Список параметрів

`values`

Значення, що додаються.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**Ds\\Queue::push()\*\*\*\*

```php
<?php
$queue = new \Ds\Queue();

$queue->push("a");
$queue->push("b");
$queue->push("c", "d");
$queue->push(...["e", "f"]);

print_r($queue);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Queue Object
(
    [0] => a
    [1] => b
    [2] => c
    [3] => d
    [4] => e
    [5] => f
)
```
