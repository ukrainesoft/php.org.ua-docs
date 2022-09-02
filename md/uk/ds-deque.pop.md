---
navigation:
  - ds-deque.merge.md: '« DsDeque::merge'
  - ds-deque.push.md: 'ДсDeque::push »'
  - index.md: PHP Manual
  - class.ds-deque.md: Двостороння черга
title: 'ДсDeque::pop'
---
# ДсDeque::pop

(PECL ds >= 1.0.0)

ДсDeque::pop — Видаляє та повертає останнє значення

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

**Приклад #1 Приклад використання **ДсDeque::pop()****

```php
<?php
$deque = new \Ds\Deque([1, 2, 3]);

var_dump($deque->pop());
var_dump($deque->pop());
var_dump($deque->pop());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(3)
int(2)
int(1)
```
