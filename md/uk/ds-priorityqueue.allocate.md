---
navigation:
  - class.ds-priorityqueue.md: « Ds\\PriorityQueue
  - ds-priorityqueue.capacity.md: 'Ds\\PriorityQueue::capacity »'
  - index.md: PHP Manual
  - class.ds-priorityqueue.md: Ds\\PriorityQueue
title: 'Ds\\PriorityQueue::allocate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\PriorityQueue::allocate

(PECL ds >= 1.0.0)

Ds\\PriorityQueue::allocate — Виділяє пам'ять під зазначену місткість

### Опис

```methodsynopsis
public Ds\PriorityQueue::allocate(int $capacity): void
```

Гарантує, що виділено достатньо пам'яті під задану місткість (кількість значень). Дозволяє уникнути динамічного перерозподілу пам'яті під час додавання значень.

### Список параметрів

`capacity`

Місткість. Очікувана кількість значень.

> **Зауваження** :
> 
> Якщо нове значення місткості менше поточного, воно не зміниться.

> **Зауваження** :
> 
> Значення місткості округляється до найближчого ступеня двійки (тобто 8, 16, 32, 64, 128 і т.д.)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** Ds\\PriorityQueue::allocate()\*\*\*\*

```php
<?php
$queue = new \Ds\PriorityQueue();
var_dump($queue->capacity());

$queue->allocate(100);
var_dump($queue->capacity());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(8)
int(128)
```
