---
navigation:
  - ds-deque.capacity.md: '« Ds\\Deque::capacity'
  - ds-deque.construct.md: 'Ds\\Deque::\_\_construct »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::clear'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::clear

(PECL ds >= 1.0.0)

Ds\\Deque::clear — Видаляє всі значення з двосторонньої черги

### Опис

```methodsynopsis
public Ds\Deque::clear(): void
```

Видаляє всі значення двосторонньої черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**Ds\\Deque::clear()\*\*\*\*

```php
<?php
$deque = new \Ds\Deque([1, 2, 3]);
print_r($deque);

$deque->clear();
print_r($deque);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Deque Object
(
    [0] => 1
    [1] => 2
    [2] => 3
)
Ds\Deque Object
(
)
```
