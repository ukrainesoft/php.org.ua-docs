---
navigation:
  - ds-deque.apply.md: '« Ds\\Deque::apply'
  - ds-deque.clear.md: 'Ds\\Deque::clear »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::capacity'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::capacity

(PECL ds >= 1.0.0)

Ds\\Deque::capacity — Повертає поточну місткість

### Опис

```methodsynopsis
public Ds\Deque::capacity(): int
```

Повертає поточну місткість.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поточна місткість.

### Приклади

**Пример #1 Пример использования**Ds\\Deque::capacity()\*\*\*\*

```php
<?php
$deque = new \Ds\Deque();
var_dump($deque->capacity());

$deque->push(...range(1, 50));
var_dump($deque->capacity());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(8)
int(64)
```
