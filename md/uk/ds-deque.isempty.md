---
navigation:
  - ds-deque.insert.md: '« Ds\\Deque::insert'
  - ds-deque.join.md: 'Ds\\Deque::join »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::isEmpty'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::isEmpty

(PECL ds >= 1.0.0)

Ds\\Deque::isEmpty — Перевіряє, чи порожня двостороння черга

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

**Пример #1 Пример использования**Ds\\Deque::isEmpty()\*\*\*\*

```php
<?php
$a = new \Ds\Deque([1, 2, 3]);
$b = new \Ds\Deque();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(false)
bool(true)
```
