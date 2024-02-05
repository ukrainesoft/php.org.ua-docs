---
navigation:
  - ds-queue.construct.md: '« Ds\\Queue::\_\_construct'
  - ds-queue.count.md: 'Ds\\Queue::count »'
  - index.md: PHP Manual
  - class.ds-queue.md: Ds\\Queue
title: 'Ds\\Queue::copy'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Queue::copy

(PECL ds >= 1.0.0)

Ds\\Queue::copy — Повертає поверхневу копію черги

### Опис

```methodsynopsis
public Ds\Queue::copy(): Ds\Queue
```

Повертає поверхневу копію черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поверхнева копія черги.

### Приклади

**Пример #1 Пример использования**Ds\\Queue::copy()\*\*\*\*

```php
<?php
$a = new \Ds\Queue([1, 2, 3]);
$b = $a->copy();

// Изменение копии не отражается на оригинале
$b->push(4);

print_r($a);
print_r($b);
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
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
)
```
