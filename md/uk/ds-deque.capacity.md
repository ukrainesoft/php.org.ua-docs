---
navigation:
  - ds-deque.apply.html: '« DsDeque::apply'
  - ds-deque.clear.html: 'ДсDeque::clear »'
  - index.html: PHP Manual
  - class.ds-deque.html: Двостороння черга
title: 'ДсDeque::capacity'
---
# ДсDeque::capacity

(PECL ds >= 1.0.0)

ДсDeque::capacity — Повертає поточну місткість

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

**Приклад #1 Приклад використання **ДсDeque::capacity()****

```php
<?php
$deque = new \Ds\Deque();
var_dump($deque->capacity());

$deque->push(...range(1, 50));
var_dump($deque->capacity());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(8)
int(64)
```
