---
navigation:
  - ds-deque.insert.html: '« DsDeque::insert'
  - ds-deque.join.html: 'ДсDeque::join »'
  - index.md: PHP Manual
  - class.ds-deque.html: Двостороння черга
title: 'ДсDeque::isEmpty'
---
# ДсDeque::isEmpty

(PECL ds >= 1.0.0)

ДсDeque::isEmpty — Перевіряє, чи порожня двостороння черга

### Опис

```methodsynopsis
public Ds\Deque::isEmpty(): bool
```

Перевіряє, чи порожня двостороння черга.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо двостороння черга порожня, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ДсDeque::isEmpty()****

```php
<?php
$a = new \Ds\Deque([1, 2, 3]);
$b = new \Ds\Deque();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(false)
bool(true)
```
