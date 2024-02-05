---
navigation:
  - ds-deque.merge.md: '« Ds\\Deque::merge'
  - ds-deque.push.md: 'Ds\\Deque::push »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::pop'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::pop

(PECL ds >= 1.0.0)

Ds\\Deque::pop — Видаляє та повертає останнє значення

### Опис

```methodsynopsis
public Ds\Deque::pop(): mixed
```

Видаляє та повертає останнє значення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останнє віддалене значення.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо колекція порожня.

### Приклади

**Приклад #1 Приклад використання** Ds\\Deque::pop()\*\*\*\*

```php
<?php
$deque = new \Ds\Deque([1, 2, 3]);

var_dump($deque->pop());
var_dump($deque->pop());
var_dump($deque->pop());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(3)
int(2)
int(1)
```
