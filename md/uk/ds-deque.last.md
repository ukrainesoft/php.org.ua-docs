---
navigation:
  - ds-deque.jsonserialize.md: '« DsDeque::jsonSerialize'
  - ds-deque.map.md: 'ДсDeque::map »'
  - index.md: PHP Manual
  - class.ds-deque.md: Двостороння черга
title: 'ДсDeque::last'
---
# ДсDeque::last

(PECL ds >= 1.0.0)

ДсDeque::last — Повертає останнє значення двосторонньої черги

### Опис

```methodsynopsis
public Ds\Deque::last(): mixed
```

Повертає останнє значення двосторонньої черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останній елемент двосторонньої черги.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо двостороння черга порожня.

### Приклади

**Приклад #1 Приклад використання **ДсDeque::last()****

```php
<?php
$deque = new \Ds\Deque([1, 2, 3]);
var_dump($deque->last());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(3)
```
