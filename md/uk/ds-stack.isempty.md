---
navigation:
  - ds-stack.count.html: '« DsStack::count'
  - ds-stack.jsonserialize.html: 'ДсStack::jsonSerialize »'
  - index.md: PHP Manual
  - class.ds-stack.html: Стек
title: 'ДсStack::isEmpty'
---
# ДсStack::isEmpty

(PECL ds >= 1.0.0)

ДсStack::isEmpty — Перевіряє, чи порожня колекція

### Опис

```methodsynopsis
public Ds\Stack::isEmpty(): bool
```

Перевіряє, чи колекція порожня.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо колекція порожня, та **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ДсStack::isEmpty()****

```php
<?php
$a = new \Ds\Stack([1, 2, 3]);
$b = new \Ds\Stack();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(false)
bool(true)
```
